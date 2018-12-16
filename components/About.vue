<template>
  <section class="about">
    <h1 class="title">About Me</h1>
    <div class="container">
      <img
        src="https://avatars0.githubusercontent.com/u/30350348?s=460&v=4" 
        alt="logo">
      <div>
        <p class="info">
          Hi I am Vaibhav Yadav, i am a self taught web developer from India. I am specialized in building Websites, Web Apps and UX Design. 
        </p>
        <h2 class="sub-title">My Skills</h2>
        <div class="skills">
          <div 
            v-for="skill in skills" 
            :key="skill.name">
            <i :class="skill.fa"/>
            <h3>{{ skill.name }}</h3>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      skills: [
        { name: "HTML", fa: "fab fa-html5" },
        { name: "CSS", fa: "fab fa-css3-alt" },
        { name: "JavaScript", fa: "fab fa-js-square" },
        { name: "Node", fa: "fab fa-node-js" },
        { name: "Vue", fa: "fab fa-vuejs" },
        { name: "React", fa: "fab fa-react" }
      ]
    }
  }
}
</script>

<style scoped>
.about {
  padding: 3rem;
  font-family: "Lobster", Arial, Helvetica, sans-serif;
  background-color: var(--primary-color);
  color: var(--secondary-color);
  text-align: center;
}

.title {
  font-size: 3.5rem;
}

.container {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  align-items: flex-start;
}

img {
  display: block;
  max-width: 200px;
  height: auto;
  border-left: 10px solid var(--secondary-color);
  border-right: 10px solid var(--secondary-color);
  border-radius: 50%;
  animation: Rotate 7s infinite alternate ease-in-out;
}

@keyframes Rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.info {
  font-size: 2.3rem;
  max-width: 700px;
  margin: 3rem auto;
}

.sub-title {
  text-align: center;
  padding-top: 4rem;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  max-width: 700px;
  margin: 2rem auto;
}

.skills div {
  margin: 2rem 5rem;
}

i {
  display: block;
  color: var(--secondary-color);
  font-size: 10rem;
}
</style>
