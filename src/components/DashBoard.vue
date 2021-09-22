<template>
  <table>
    <tr>
      <th>Id</th>
      <th>Name</th>
      <th>Point</th>
    </tr>
    <tr v-for="(user, i) in players" :key="i">
      <td>2</td>
      <td>{{ user.name }}</td>
      <td>{{ user.score }}</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Tim Cook</td>
      <td>45</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Ernst Handel</td>
      <td>40</td>
    </tr>
  </table>
</template>
<script>
export default {
  name: "LeaderBoard",
  inject: ["players"],
};
</script>
