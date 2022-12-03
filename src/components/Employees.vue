<template>
  <v-table class="employeestable">
    <thead>
      <tr>
        <th class="text-center">
          Name
        </th>
        <th class="text-center">
          Email
        </th>
        <th class="text-center">
          performance
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="employee in (SearchingEmployee.length !== 0 || (SearchingEmployee.length === 0 && userValue.length > 0) ? SearchingEmployee : employees)"
        :key="employee.id"
      >
        <td class="text-center">{{ employee.profile.name }}</td>
        <td class="text-center">{{ employee.email }}</td>
        <td class="text-center">{{ Number.isInteger(employee.performance_index*100)? employee.performance_index*100+"%": Math.round(employee.performance_index *100)+"%" }}</td>
      </tr>
    </tbody>
  </v-table>
</template>

<script>
  export default {
    props: [
      'employees',
      'SearchingEmployee',
      'userValue'
    ]
  }
</script>

<style scoped>
.employeestable {
  margin-bottom: 2rem;
}
</style>


// desserts: [
//   {
//     name: 'Frozen Yogurt',
//     email: 'frozen_mueller@zesla.com',
//     performance: '10%',
//   },
//   {
//     name: 'Moses Mueller',
//     email: 'moses_mueller@zesla.com',
//     performance: '70%',
//   },
//   {
//     name: 'Durham Ross',
//     email: 'durham_ross@zesla.com',
//     performance: '30%',
//   },
//   {
//     name: 'Penny Alexander',
//     email: 'penny_alexander@zesla.com',
//     performance: '15%',
//   },
//   {
//     name: 'Rose Morrison',
//     email: 'rose_morrison@zesla.com',
//     performance: '60%',
//   },
//   {
//     name: 'Ethel Adkins',
//     email: 'ethel_adkins@zesla.com',
//     performance: '12%',
//   },
// ],