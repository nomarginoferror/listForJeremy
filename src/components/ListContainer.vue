<template>
  <div>
    <form @submit="addTodo">
      <div class="hello">
        <div class="parallel-div">
          <h3>Name</h3>
          <input type="text" v-model="name" />
        </div>
        <div class="parallel-div">
          <h3>D.O.B.</h3>
          <input type="text" v-model="dob" />
        </div>
        <div class="parallel-div">
          <h3>Email</h3>
          <input type="text" v-model="email" />
        </div>
        <div class="parallel-div">
          <input type="submit" placeholder="submit" />
        </div>
      </div>
    </form>
    <Items v-bind:people="people" />
  </div>
</template>

<script>
import Items from "./Items.vue";

export default {
  name: "ListContainer",
  components: {
    Items
  },
  data() {
    return {
      people: []
    };
  },
  methods: {
    clearFields() {
      this.name = "";
      this.dob = "";
      this.email = "";
    },
    addTodo(e) {
      e.preventDefault();
      const newPerson = {
        id: Date.now(),
        name: this.name,
        dob: this.dob,
        email: this.email
      };
      this.people = [...this.people, newPerson];
      this.clearFields();
    }
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  display: flex;
  width: 100%;
  justify-content: center;
}
.parallel-div {
  display: inline;
  margin: 0 2rem;
}
h3 {
  margin: 0;
  display: inline;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
