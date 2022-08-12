<template>
  <table border="2px solid">
    <th>id</th>
    <th>name</th>
    <th>age</th>
    <tr v-for="user in users" :key="user.id">
    <td>{{user.id}}</td>
    <td>{{user.name}}</td>
    <td>{{user.age}}</td>
    </tr>
  </table>
</template>
<script>
export default {
  data() {
    return {
      users: [
        { name: "kanon", id: 1, age: 30 },
        { name: "kpol", id: 2, age: 22 },
        { name: "ayon", id: 3, age: 17 },
        { name: "mukti", id: 4, age: 30 },
      ],
    };
  },
};
</script>