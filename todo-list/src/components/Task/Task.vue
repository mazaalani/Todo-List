<template>
  <div class="mt-3">
    <div class="card">
      <h4 class="p-3">{{ titre }}</h4>
      <button class="btn btn-danger" @click="deleteTask">X</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Task",
  data() {
    return {};
  },
  props: ["titre", "deleteTask"],
  methods: {
    delTask: function() {
      this.$emit("delTask", this.titre);
    },
  },
};
</script>

<style scoped src="./Task.css"></style>
