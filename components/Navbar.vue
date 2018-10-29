<template>
  <nav class="navbar">
    <div class="head-nav">
      <a 
        href="#" 
        class="logo">Vaibhav Yadav</a>

      <div class="desk-navs">
        <a 
          v-for="link in links" 
          :key="link.name" 
          :href="link.href"
          class="nav-link"> {{ link.name }} </a>
      </div>

      <i 
        class="fas fa-bars fa-2x menu-btn" 
        @click="show = !show" />
    </div>

    <div 
      :class="{show: show}"
      class="mobile-navs" 
    >
      <a 
        v-for="link in links" 
        :key="link.name" 
        :href="link.href"
        class="nav-link"> {{ link.name }} </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      links: [
        { name: "Home", href: "#" },
        { name: "Projects", href: "#projects" },
        { name: "About", href: "#about" }
      ],
      show: false
    }
  }
}
</script>

<style scoped>
.navbar {
  width: 100%;
  top: 0;
  background-color: var(--primary-color);
  color: var(--secondary-color);
  position: fixed;
  overflow: hidden;
}

.head-nav,
.desk-navs {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}

.head-nav {
  width: 80%;
  margin: 0 auto;
}

.logo,
.nav-link {
  display: block;
  text-decoration: none;
  color: var(--secondary-color);
  margin: 1rem;
}

.logo {
  font-family: "Lobster", cursive, Arial, sans-serif;
  font-size: 2rem;
  font-weight: 800;
}

.nav-link {
  padding: 1rem;
  transition: all 0.2s;
}

.nav-link:hover {
  color: black;
  background-color: var(--secondary-color);
  border-radius: 1rem;
}

.menu-btn {
  color: var(--secondary-color);
  cursor: pointer;
  margin: 1rem;
  display: none;
}

.mobile-navs {
  width: 100%;
  text-align: center;
  display: none;
}

.show {
  display: block;
}

@media only screen and (max-width: 700px) {
  .head-nav {
    width: 100%;
  }

  .desk-navs {
    display: none;
  }

  .menu-btn {
    display: block;
  }
}

@media only screen and (min-width: 701px) {
  .mobile-navs {
    display: none;
  }
}
</style>
