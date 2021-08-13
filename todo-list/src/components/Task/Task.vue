<template>
  <div class="mt-3">
    <div class="card">
      <h3 class="p-3">{{ titre }}</h3>
      <button class="btn btn-danger" @click="delTask">X</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Task",
  data() {
    return {};
  },
  props: ["titre"],
  methods: {
    delTask: function() {
      this.$emit("delTask", this.titre);
    },
  },
};
</script>

<style scoped src="./Task.css"></style>
