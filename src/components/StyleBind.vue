<template>
  <div>
    <h1>样式绑定</h1>
    <p :style="{ color: color, fontSize: fontSize }">这是一段红色的文字</p>
    <p :style="styleObject">这是一段蓝色的文字</p>
    <p :class="{ active: isActive }" class="basic-style">
      这是一段带有active类的文字
    </p>
    <input type="button" value="Toggle Active" @click="toggleActive" />
  </div>
</template>

<script>
export default {
  name: "StyleBind",
  data() {
    return {
      color: "red",
      fontSize: "30px",
      isActive: true,
      styleObject: {
        color: "blue",
        fontSize: "40px",
      },
    };
  },
  methods: {
    toggleActive() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
.basic-style {
  color: green;
  font-size: 30px;
}
.active {
  font-weight: bold;
}
</style>
