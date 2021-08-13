<template>
  <div class="header-top">
    <p>{{ titre }}</p>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      titre: "Todo List",
    };
  },
};
</script>
<style scoped>
.header-top {
  position: fixed;
  top: 0;
  width: 100%;
  height: 50px;
  background: #333;
  color: white;
  text-align: center;
  line-height: 50px;
  font-size: 25px;
}
</style>
