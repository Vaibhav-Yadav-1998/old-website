<template>
  <div class="welcome">
    <h1 class="heading">Welcome &#x1F64F; <br> I am Vaibhav</h1>
    <a 
      href="#about" 
      class="about-me">About Me</a>
  </div>
</template>

<script>
export default {
  name: "Welcome"
}
</script>

<style scoped>
.welcome {
  background: url("../assets/showcase.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  width: 100%;
  height: 100vh;
  background-position: center;
  color: white;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.heading {
  font-size: 6rem;
  font-family: "Lobster", Arial, Helvetica, sans-serif;
  background: rgba(65, 65, 65, 0.3);
  border-radius: 1rem;
}

.about-me {
  padding: 1rem;
  margin: 2rem;
  background-color: var(--primary-color);
  color: var(--secondary-color);
  text-decoration: none;
  border-radius: 1rem;
  transition: all 0.3s;
}

.about-me:hover {
  background-color: var(--secondary-color);
  color: black;
  padding: 1rem 1.5rem;
  border-radius: 1.5rem;
  border: 0.5rem solid var(--primary-color);
  font-weight: 800;
}

@media only screen and (max-width: 500px) {
  .heading {
    font-size: 4rem;
  }
}
</style>
