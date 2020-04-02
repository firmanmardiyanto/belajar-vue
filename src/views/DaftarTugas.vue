<template>
   <div id="app">
    <h4 class="text-center bg-primary text-white p-2">
      Daftar Tugas {{name}}
    </h4><br>
    <div class="container-fluid p-4">
      <div class="row">
        <div class="col font-weight-bold">Tugas</div>
        <div class="col-2 font-weight-bold">Selesai</div>
      </div>
      <div class="row" v-for="t in filteredTasks" v-bind:key="t.action">
        <div class="col">{{t.action}}</div>
        <div class="col-2 text-left">
          <input type="checkbox" v-model="t.done" class="form-check-input" />  {{t.done}}
        </div>
      </div>
      <div class="row py-2">
        <div class="col">
          <input v-model="newItemText" class="form-control" />
        </div>
        <div class="col-2">
          <button class="btn btn-primary" v-on:click="addNewToDo">Tambah</button>
        </div>
      </div>
        <div class="row bg-secondary py-2 mt-2 text-white">
          <div class="col text-center">
          <input type="checkbox" v-model="hideCompleted" class="form-check-input" />
          <label class="form-check-label font-weight-bold">
            Hide completed tasks
          </label>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DaftarTugas',
  props: {
    msg: String
  },
   data() {
      return {
        name: "Firman",
        tasks: [{action: "Beli Cincin", done: false},
                {action: "Beli Kue", done: false},
                {action: "Kerjain Tugas", done: true},
                {action: "Kabarin Pacar", done: true}],
        hideCompleted: true,
        newItemText: ""
      }
    },
    computed: {
      filteredTasks() {
        return this.hideCompleted ?
          this.tasks.filter(t => !t.done) : this.tasks
      }
    },
    methods: {
      addNewToDo() {
        this.tasks.push({
          action: this.newItemText,
          done: false
        });
        this.newItemText = "";
      }
    }
}
</script>