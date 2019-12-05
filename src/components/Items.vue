<template>
  <div>
    <table>
      <tbody v-bind:key="people.id" v-for="people in people">
        <Item v-bind:people="people" />
      </tbody>
    </table>
  </div>
</template>

<script>
import Item from "./Item.vue";

export default {
  name: "Items",
  props: ["people"],
  components: {
    Item
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
table {
  margin: 2rem auto;
  border-collapse: collapse;
  border-radius: 0.2rem;
  margin-bottom: 1rem;
  color: #495057;
  width: 50rem;
  align-content: center;
  justify-content: center;
  justify-items: center;
}

tr {
  width: 100%;
  border-bottom: 1px solid #dfdfdf;
  transition: 0.1s;
}

tbody tr:hover {
  color: black;
}

th,
td {
  text-align: center;
  margin: auto;
}

table th,
table td {
  vertical-align: top;
}

table thead th {
  vertical-align: bottom;
}

table tbody + tbody {
  border-top: 2px solid #dee2e6;
}
</style>
