<template>
  <div>
    <h1>列表渲染</h1>
    <ul>
      <li v-for="item in list" :key="item.id">
        <span>{{ item.id }}</span>
        <span>{{ item.name }}</span>
        <span>{{ item.age }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ListRender",
  components: {},
  data() {
    return {
      list: [
        { id: 1, name: "张三", age: 20 },
        { id: 2, name: "李四", age: 21 },
        { id: 3, name: "王五", age: 22 },
        { id: 4, name: "赵六", age: 23 },
      ],
    };
  },
};
</script>

<style scoped></style>
