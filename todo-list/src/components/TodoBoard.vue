<template>
  <div class="container mt-5">
    <h1>Enter Task</h1>

    <form>
      <div class="form-group">
        <label for="action">Action</label>
        <input v-model="action" type="text" id="action" class="form-control" />
      </div>

      <button @click.prevent="createTask" class="btn btn-primary mt-3">
        Create Task
      </button>
    </form>

    <div>
      <task
        v-bind:key="index"
        v-for="(task, index) in titre"
        :titre="task"
        :id="index"
        :deleteTask="deleteTask"
      ></task>
    </div>
  </div>
</template>

<script>
import Task from "./Task/Task.vue";

export default {
  name: "TodoBoard",
  data() {
    return {
      action: "",
      titre: ["Javascript", "VueJs", "CSS", "HTML"],
    };
  },
  components: {
    task: Task,
  },
  methods: {
    createTask: function() {
      this.titre.push(this.action);
      this.action = "";
    },
    deleteTask: function(e) {
      this.titre.splice(e.target.parentNode.parentNode.id, 1);
    },
  },
};
</script>

<style></style>
