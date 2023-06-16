<template>
  <div class="row">
    <div class="col-12 mb-4">
      <h3 class="text-center">Progress: 0%</h3>
      <div class="progress">
        <div 
        class="progress-bar progress-bar-striped  progress-bar-animated bg-success"
        role="progressbar"
        aria-valuenow="25"
        aria-valuemin="0%"
        aria-valuemax="100%"
        style="width : 75%;"
        ></div>
      </div>
    </div>
    <div class="col-12 col-md-4">
      <form @submit.prevent="registerProject()">
        <div class="mb-3">
          <label for="form-label">Project</label>
          <input v-model.trim="project" type="text" class="form-control" required />
        </div>
        <div class="mb-3">
          <label for="form-label">Activity</label><br>
          <select v-model="type" class="form-select" required>
            <option disabled selected value="">Select a type</option>
            <option>Web Aplication with Vue.js</option>
            <option>Backent sevice Node.js</option>
            <option>App Movile with React Native</option>
          </select>
        </div>
        <div class="mb-3">
          <label class="form-check-label"> Urgent </label> <br>
          <input v-model="checkbox" type="checkbox" form="form-check-input" />
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>
    <div class="col-12 col-md-8">
      <h3>All Projects: {{ nameProject }}</h3>
      <div class="table-responsive">
        <table class="table table-dark table-hover">
          <thead>
            <tr>
              <th>#</th>
              <th>Project</th>
              <th>Type</th>
              <th>Urgent</th>
              <th>Completed</th>
            </tr>
          </thead>

          <tbody>
            <tr v-for="(project, index) in projects" :key="index">
              <td>{{ index + 1 }}</td>
              <td>{{ project.project }}</td>
              <td>{{ project.type }}</td>
              <td @click="changeState(index)" :class="project.checkbox ? 'bg-success' : 'bg-danger'">
                {{ project.checkbox ? "SI" : "NO" }}
              </td>
              <td @click="changeCompleted(index)" :class="project.completed ? 'bg-success' : 'bg-danger'">
                {{ project.completed ? "DONE" : "INCOMPLETE" }}
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    project: "",
    type: "",
    checkbox: false,
    completed: false,
    projects: [],
  }),
  methods: {
    registerProject() {

      //completado false
      const project = {
        project: this.project,
        type: this.type,
        checkbox: this.checkbox,
        completed: this.completed
      }

      this.projects.push(project)

      this.project = ""
      this.type = ""
      this.checkbox = false
      this.completed = false
    },
    changeState(id) {
      this.projects[id].checkbox = !this.projects[id].checkbox
    },
    changeCompleted(id){
      this.projects[id].completed = !this.projects[id].completed 
    }
  },
  computed: {
    nameProject() {
      return this.projects.length
    }
  }
};
</script>