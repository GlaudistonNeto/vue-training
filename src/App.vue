<template>
  <FirstComponent msg="Welcome to Your Vue.js App"/>
  <LifeCycle />
  <Person />
  <Form />
</template>

<script>
import FirstComponent from './components/FirstComponent.vue';
import LifeCycle from './components/LifeCycle.vue';
import Person from './components/Person.vue';

export default {
  name: 'App',
  components: {
    FirstComponent,
    LifeCycle,
    Person,
  }
}
</script>

    LifeCicle
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
