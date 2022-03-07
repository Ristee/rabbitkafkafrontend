<template>
  <p v-if="name">
    Using <span class="api-name">{{ name }}</span> version {{ version }}<br>
    URL: <a :href="baseUrl">{{ baseUrl }}</a>
  </p>
  <p v-else>
    Loading...
  </p>
</template>

<script>
import axios from 'axios';

export default {
  name: "ApiStatus",
  data() {
    return {
      name: null,
      version: null,
      baseUrl: null,
    }
  },
  mounted() {
    axios.get('/').then(response => {
      this.name = response.data.name;
      this.version = response.data.version;
      this.baseUrl = axios.defaults.baseURL;
    })
  },
}
</script>

<style scoped lang="scss">
.api-name {
  font-weight: bold;
}
</style>