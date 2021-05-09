<template>
  <section id="app">
    <Home />
  </section>
</template>

<script>
import Home from "./components/Home"

export default {
  name: 'App',

  components: {
    Home
  },

  data() {
    return {

    }
  }
};
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: 'Open Sans', sans-serif;
}
</style>