<template>
  <div>
    <h1>基本用法测试</h1>
    <p>{{ msg }}</p>
    <input v-model="msg" />
    <button @click="reverseString">反转字符串</button>
    <p>{{ firstName }} + {{ lastName }} => {{ fullName }}</p>
  </div>
</template>

<script>
export default {
  name: "BasicComponents",
  components: {},
  data() {
    return {
      msg: "Hello Vue!",
      firstName: "John",
      lastName: "Doe",
    };
  },
  computed: {
    fullName: {
      // Getter
      get() {
        return this.firstName + " " + this.lastName;
      },
      // Setter
      set(newValue) {
        const names = newValue.split(" ");
        this.firstName = names[0];
        this.lastName = names[names.length - 1];
      },
    },
  },
  methods: {
    reverseString: function () {
      this.msg = this.msg.split("").reverse().join("");
    },
  },
  watch: {
    // 监听msg变化
    msg: function (newVal, oldVal) {
      console.log("msg changed from " + oldVal + " to " + newVal);
    },
  },
};
</script>

<style scoped></style>
