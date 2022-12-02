<template>
  <v-table>
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
        v-for="item in desserts"
        :key="item.name"
      >
        <td class="text-center">{{ item.name }}</td>
        <td class="text-center">{{ item.email }}</td>
        <td class="text-center">{{ item.performance }}</td>
      </tr>
    </tbody>
  </v-table>
</template>

<script>
  export default {
    data () {
      return {
        desserts: [
          {
            name: 'Frozen Yogurt',
            email: 'frozen_mueller@zesla.com',
            performance: '10%',
          },
          {
            name: 'Moses Mueller',
            email: 'moses_mueller@zesla.com',
            performance: '70%',
          },
          {
            name: 'Durham Ross',
            email: 'durham_ross@zesla.com',
            performance: '30%',
          },
          {
            name: 'Penny Alexander',
            email: 'penny_alexander@zesla.com',
            performance: '15%',
          },
          {
            name: 'Rose Morrison',
            email: 'rose_morrison@zesla.com',
            performance: '60%',
          },
          {
            name: 'Ethel Adkins',
            email: 'ethel_adkins@zesla.com',
            performance: '12%',
          },
        ],
      }
    },
  }
</script>