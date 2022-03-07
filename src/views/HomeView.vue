<template>
  <div class="home">
    <div class="jumbotron">
      <h1>Welcome App</h1>
      <p>Congratualtion!</p>
    </div>
    <ApiStatus/>
  </div>
</template>

<script>
// @ is an alias to /src
import ApiStatus from "@/components/ApiStatus";

export default {
  components: {
    ApiStatus
  },
  name: 'HomeView'
}
</script>

<style lang="scss">

</style>
