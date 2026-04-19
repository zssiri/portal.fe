<template>
  <nav class="navbar bg-body-tertiary">
    <div class="container-fluid">
      <router-link class="navbar-brand" :to="{name: 'Main'}">NewsPortal</router-link>
    </div>
  </nav>

  <div class="container">
    <RouterView />
  </div>
</template>

<script>
export default {

}
</script>

<style scoped></style>
