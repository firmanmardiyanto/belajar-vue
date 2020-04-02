<template>
  <div id="app ">
    <h1 class="p-2 text-center">
      <router-link class="btn btn-primary text-white bg-primary" to="/">--BERANJEUN--</router-link>
    </h1>
      <div><router-view/></div>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>
