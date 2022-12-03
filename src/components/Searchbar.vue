<template>
    <div class="searchbar">
      <font-awesome-icon icon="fa-solid fa-magnifying-glass" class="searchicon"/>
      <input type="text" class="searchbtn" placeholder="Search Here"
       v-model="userValue" @keyup="filterEmployees(userValue)"
      />
    </div>
</template>

<script>
export default {
    props: ['filterEmployees']
}
</script>

<style>
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
@media (max-width: 575px) {
  .searchbar {
    max-width: 100%;
  }
}
</style>