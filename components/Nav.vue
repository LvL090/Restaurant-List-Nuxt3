<template lang="pug">
nav.navbar.navbar-expand-lg.navbar-dark.bg-dark
  .container-fluid
    a.navbar-brand(href="/") Restaurantly
    #navbarSupportedContent.collapse.navbar-collapse
      ul.navbar-nav.ml-auto.mb-2.mb-lg-0
        li.nav-item
          a.nav-link.active(aria-current="page" href="/") Home
        li.nav-item
          a.nav-link(href="/restaurants") Restaurants
</template>

<style scoped>
.ml-auto {
  margin-left: auto;
}
</style>
