<template>
  <div class="parent-container">
    <h2>父组件</h2>
    <p>父组件消息：{{ parentMessage }}</p>
    <ChildComponent
      :id="1"
      :message="parentMessage"
      @childChange="childMessageChange"
    />
    <p>来自子组件的消息：{{ childMessage }}</p>
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";

export default {
  name: "ParentComponent",
  components: {
    ChildComponent,
  },
  data() {
    return {
      parentMessage: "Hello from parent",
      childMessage: "",
    };
  },
  methods: {
    childMessageChange(message) {
      this.childMessage = message;
    },
  },
  beforeCreate() {
    console.log("ParentComponent beforeCreate");
  },
  created() {
    console.log("ParentComponent created");
  },
  beforeMount() {
    console.log("ParentComponent beforeMount");
  },
  mounted() {
    console.log("ParentComponent mounted");
  },
  beforeUpdate() {
    console.log("ParentComponent beforeUpdate");
  },
  updated() {
    console.log("ParentComponent updated");
  },
  beforeDestroy() {
    console.log("ParentComponent beforeDestroy");
  },
  destroyed() {
    console.log("ParentComponent destroyed");
  },
};
</script>

<style scoped>
.parent-container {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
