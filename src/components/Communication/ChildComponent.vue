<template>
  <div class="child-container">
    <h2>子组件{{ id }}</h2>
    <p>子组件接收到父组件消息：{{ message }}</p>
    <input type="text" v-model="childMessage" />
    <input type="button" value="Send Message" @click="sendMessage" />
  </div>
</template>

<script>
export default {
  props: ["id", "message"],
  name: "ChildComponent",
  data() {
    return {
      childMessage: "",
    };
  },
  methods: {
    sendMessage() {
      this.$emit("childChange", this.childMessage);
    },
  },
  beforeCreate() {
    console.log("ChildComponent beforeCreate");
  },
  created() {
    console.log("ChildComponent created");
  },
  beforeMount() {
    console.log("ChildComponent beforeMount");
  },
  mounted() {
    console.log("ChildComponent mounted");
  },
  beforeUpdate() {
    console.log("ChildComponent beforeUpdate");
  },
  updated() {
    console.log("ChildComponent updated");
  },
  beforeDestroy() {
    console.log("ChildComponent beforeDestroy");
  },
  destroyed() {
    console.log("ChildComponent destroyed");
  },
};
</script>

<style scoped>
.child-container {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
