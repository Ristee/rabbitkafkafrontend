<template>
  <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white border-bottom box-shadow fixed-top">
    <h5 class="my-0 mr-md-auto font-weight-normal">
      <router-link :to="{name: 'home'}">App name</router-link>
    </h5>
    <router-link class="p-2 text-dark" :to="{name: 'about'}">About</router-link>
    <nav class="my-2 my-md-0 mr-md-3">
      <a class="p-2 text-dark" href="#">Sign In</a>
    </nav>
    <a class="btn btn-outline-primary" href="#">Sign up</a>
  </div>
</template>

<script>
export default {
  name: 'NavLinks'
}
</script>

<style scoped lang="scss">

</style>