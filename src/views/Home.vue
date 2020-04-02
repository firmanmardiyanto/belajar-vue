<template>
  <div id="app">
    <div id="nav" class="row">
      <router-link class="col btn btn-success" to="/DaftarTugas">Daftar Tugas (ToDo)</router-link> <br>
      <router-link class="col-2 btn btn-secondary" to="/DataDiri">Data Diri</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>
