<template>
  <div class="root-container">
    <h1>父子组件通信</h1>
    <ParentComponent v-if="isShow" />
    <input type="button" :value="buttonText" @click="toggleComponent" />
  </div>
</template>

<script>
import ParentComponent from "./ParentComponent.vue";
export default {
  name: "CommunicationTest",
  components: {
    ParentComponent,
  },
  data() {
    return {
      isShow: false,
    };
  },
  methods: {
    toggleComponent() {
      this.isShow = !this.isShow;
    },
  },
  computed: {
    buttonText() {
      return this.isShow ? "销毁" : "创建";
    },
  },
};
</script>

<style lang="scss" scoped></style>
