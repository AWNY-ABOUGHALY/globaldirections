<script setup>
import Employees from './components/Employees.vue'
</script>

<template>
  <div class="container">
    <header>
      <img alt="three-sixty logo" class="logo" src="./assets/logo.png"/>
    </header>

    <div class="Employees">
      <Employees />
    </div>
  </div>
  <main>

  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
  padding: 1rem 0;
}

.container {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 1rem;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
   /* Better to move these flex code to the header in global and remove it from here
      then also remove the margin of logo from global and media query, so we will just have 
      one code for centering */
    display: flex;
    place-items: center;
    justify-content: center;
    background: #ccc;
  }

  .logo {
    /* I think it supposed to be (margin: 0 0 2rem 0;)
       that means margin-bottom: 2rem; */
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
