<template>
  <form @submit.prevent="registerProject()">
    <div class="mb-3">
      <label for="form-label">Project</label>
      <input v-model.trim="nameProject" type="text" class="form-control" required />
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
  <h3>All Projects: {{ nameProject }}</h3>
  <div class="table-responsive">
    <table class="table table-dark table-hover">
      <thead>
        <tr>
          <th>#</th>
          <th>Project</th>
          <th>Type</th>
          <th>Urgent</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="(project, index) in projects" :key="index">
          <td>{{ index + 1}}</td>
          <td>{{ project.project }}</td>
          <td>{{ project.type}}</td>
          <td :class=" project.checkbox ? 'bg-success' : 'bg-danger' ">{{ project.checkbox ? "SI" : "NO" }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data: () => ({
    project: "",
    type: "",
    checkbox: false,
    projects: [],
  }),
  methods: {
    registerProject() {
      const project = {
        project: this.project,
        type: this.type,
        checkbox: this.checkbox,
      }

      this.projects.push(project)

      this.project = ""
      this.type = ""
      this.checkbox = false
    },
  },
  computed: {
    nameProject(){
      return this.projects.length
    }
  }
};
</script>