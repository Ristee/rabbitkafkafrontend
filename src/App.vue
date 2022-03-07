<template>
  <div id="app">
    <header class="app-header">
      <NavLinks/>
    </header>
    <div class="app-content">
      <main class="container">
        <router-view/>
      </main>
    </div>
    <footer>
      <div class="container">
        <hr/>
        <p>&copy; App. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<script>
import NavLinks from "@/components/NavLinks";

export default {
  components: {
    NavLinks
  }
}
</script>

<style lang="scss">
@import "assets/scss/variables";
@import "~bootstrap/scss/bootstrap";
@import "~bootstrap-vue/dist/bootstrap-vue.css";
@import "~@fortawesome/fontawesome-free/css/all.css";

body {
  min-height: 85vh;
  padding-top: 5rem;
}

html {
  position: relative;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  min-height: 85vh;
  display: flex;
  flex-direction: column;
}

.app-content {
  flex: 1;
  padding: 1rem 0;
}


.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  /* Set the fixed height of the footer here */
  height: 60px;
  line-height: 60px; /* Vertically center the text there */
  background-color: #f5f5f5;
}

body > .container {
  padding: 60px 15px 0;
}

.footer > .container {
  padding-right: 15px;
  padding-left: 15px;
}

code {
  font-size: 80%;
}

</style>
