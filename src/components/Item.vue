<template>
  <tr>
    <td>{{people.name}}</td>
    <td>{{people.dob}}</td>
    <td>{{people.email}}</td>
  </tr>
</template>

<script>
export default {
  name: "Item",
  props: ["people"]
};
</script>


