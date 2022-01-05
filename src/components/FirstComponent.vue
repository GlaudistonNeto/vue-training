<template>
  <div>
    <h1>Hello vue!</h1>
    <p>My name is {{ name }}</p>
    <p>My work is: {{ profession }}</p>
    <MultipleEvents />
    <TheReuse />
  </div>
</template>

<script>
import MultipleEvents from './MultipleEvents.vue';
import TheReuse from './TheReuse.vue';

export default {
  components: {
    MultipleEvents,
    TheReuse,
  },
  data() {
    return {
      name: "G-Neto",
      profession: "software developer"
    }
  },
  name: 'FirstComponent',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
