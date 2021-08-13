<template>
  <div id="app">
    <HeaderTop></HeaderTop>
    <TodoBoard></TodoBoard>
  </div>
</template>

<script>
import HeaderTop from "./components/HeaderTop.vue";
import TodoBoard from "./components/TodoBoard.vue";

export default {
  name: "App",
  components: {
    TodoBoard,
    HeaderTop,
  },
};
</script>

<style></style>
