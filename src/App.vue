<script setup>
import Employees from './components/Employees.vue'
import Searchbar from './components/Searchbar.vue'
</script>

<template>
  <div class="container">
    <header>
      <img alt="three-sixty logo" class="logo" src="./assets/logo.png"/>
    </header>
    <Searchbar :filterEmployees="filterEmployees"/>
    <Employees :employees="employees" :SearchingEmployee="SearchingEmployee" :userValue="userValue"/>
  </div>
</template>

<script>
import axios from 'axios';
export default {
    data () {
      return {
        employees: [],
        SearchingEmployee: [],
        userValue: ''
      }
    },
    mounted(){
      axios.get("https://fe-task.getsandbox.com/employees")
      .then(res=> this.employees = res.data.employees)
    },
    methods: {
      filterEmployees(userValue){
        this.userValue = userValue
        this.SearchingEmployee = this.employees.filter((employee)=>{
          return employee.profile.name.includes(userValue) || employee.email.includes(userValue)
        })
      }
    }
  }
</script>

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
}
</style>
