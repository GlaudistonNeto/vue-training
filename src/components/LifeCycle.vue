<template>
  <div>
    <p>My name is {{ name }}</p>
  </div>
</template>

<script>
export default {
  name: 'LifeCycle',
  data() {
    return {
      name: "Something"
    }
  },
  created() {
    setTimeout(() => {
      this.name = "G.S.O.Neto"      
    }, 1000);

    this.lifeCycle();
  },
  mounted() {
    setTimeout(() => {      
      this.name = "Other cat"
    }, 2000);

    this.lifeCycle();
  },
  methods: {
    lifeCycle() {
      console.log('Executed!');
    }
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
