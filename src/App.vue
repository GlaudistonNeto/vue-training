<template>
  <Header />
  <FirstComponent msg="Welcome to Your Vue.js App"/>
  <LifeCycle />
  <Person />
  <Form />
</template>

<script>
import FirstComponent from './components/FirstComponent.vue';
import Header from './components/Header.vue';
import LifeCycle from './components/LifeCycle.vue';
import Person from './components/Person.vue';

export default {
  name: 'App',
  components: {
    FirstComponent,
    LifeCycle,
    Person,
    Header,
  }
}
</script>

    LifeCicle
<style>
body {
  background-color: #333;
  color: #fff;
}
a {
  color: rgba(17, 191, 197, 0.863);
}
a:hover {
  color: #ffff00
}
</style>
