<template>
  <main>
    <Navbar />
    <div id="wrapper">
      <nuxt />
    </div>
  </main>
</template>

<script>
import Navbar from "../components/Navbar"

export default {
  components: {
    Navbar
  }
}
</script>

<style>
:root {
  font-size: 62.5%;
  --primary-color: #6b238e;
  --secondary-color: #eee;
}

body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  font-size: calc(1.6rem + (2 - 1.6) * ((100vw - 32rem) / (160 - 32)));
}

#wrapper {
  padding-top: 5rem;
}
</style>
