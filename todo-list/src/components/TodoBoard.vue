<template>
  <div class="container">
    <h1>Rentrez vos choses à faire.</h1>

    <form>
      <div class="form-group">
        <label for="action">Action</label>
        <input v-model="action" type="text" id="action" class="form-control" />
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "TodoBoard",
  data() {
    return {
      action: "",
    };
  },
};
</script>

<style></style>
