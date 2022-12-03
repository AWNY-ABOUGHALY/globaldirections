<script setup>
import Employees from './components/Employees.vue'
</script>

<template>
  <div class="container">
    <header>
      <img alt="three-sixty logo" class="logo" src="./assets/logo.png"/>
    </header>
    <div class="searchbar">
      <font-awesome-icon icon="fa-solid fa-magnifying-glass" class="searchicon"/>
      <input type="text" class="searchbtn" placeholder="Search Here"/>
    </div>
    <div class="Employees">
      <Employees />
    </div>
  </div>
</template>

<style scoped>
header {
  display: flex;
  justify-content: flex-start;
  padding: 2.5rem 0;
}

.container {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 1rem;
}

.searchbar {
  position: relative;
  max-width: 15rem;
  margin: 1rem 0;
  display: flex;
  justify-content: flex-start;
  place-items: center;
}
.searchbtn {
  width: 100%;
  background-color: #fffae6;
  border-radius: 1.5rem;
  padding: 0.7rem 0.7rem 0.7rem 2.7rem;
}
.searchbtn::placeholder {
  font-size: 12px;
  font-weight: bold;
  color: #001658;
}
.searchbtn:focus {
  outline: none;
}
.searchicon {
  position: absolute;
  margin-left: 1rem;
  color: #001658;
  font-size: 20px;
}

/* @media (min-width: 1024px) {
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
@media (max-width: 575px) {
  header {
    justify-content: center;
  }
  .searchbar {
    max-width: 100%;
  }
}
</style>
