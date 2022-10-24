<template lang="pug">
div
  .container
    h1 Welcome to Restaurantly
    NuxtLink(to="/restaurants")
      button.btn.btn-outline-primary(type="button") Go to restaurants
</template>

<style scoped>
.container {
  text-align: center;
  margin-top: 3rem;
}
</style>
