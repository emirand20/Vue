<template>
  <form @submit.prevent="registerProject()">
    <div class="mb-3">
      <label for="form-label">Project</label>
      <input v-model.trim="project" type="text" class="form-control" required />
    </div>
    <div class="mb-3">
      <label for="form-label">Activity</label>
      <select v-model="type" class="form-select" required>
        <option disabled selected value="">Select a type</option>
        <option>Web Aplication with Vue.js</option>
        <option>Backent sevice Node.js</option>
        <option>App Movile with React Native</option>
      </select>
    </div>
    <div class="mb-3">
      <label class="form-check-label"> Urgent </label>
      <input v-model="checkbox" type="checkbox" form="form-check-input" />
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
  <hr />
  <pre>
        PROJECT: {{ project }} 
        TYPE: {{ type }} 
        CHECKBOX: {{ checkbox }}
    </pre
  >
</template>

<script>
export default {
  data: () => ({
    project: "",
    type: "",
    checkbox: false,
  }),
  methods: {
    registerProject() {
      console.log(this.project);
    },
  },
};
</script>