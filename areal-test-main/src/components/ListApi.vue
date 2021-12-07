<template>
      <tr>
        <td> {{ list['id'] }}</td>
        <td> {{ list['first_name'] }}</td>
        <td> {{ list['last_name'] }}</td>
        <td> {{ list['email'] }}</td>
      </tr>
</template>

<script>
export default {
  props: ["list"],
  data() {
    return {
    }
  },
}
</script>

<style>
td {
  border: 2px solid grey;
  padding: 10px;
  border-radius: 5px;
}

</style>