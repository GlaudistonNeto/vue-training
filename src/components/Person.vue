<template>
  <div>
    <h2>This is the person decription: {{ name }}</h2>
    <Info :email="email" :isWorking=false />
    <Form />
  </div>
</template>

<script>
import Info from './Info.vue';
import Form from './Form.vue';

export default {
  name: 'Person',
  data() {
    return {
      name: 'G-Neto',
      email: 'glaudistonson@gmail.com'
    }
  },
  components: {
    Info,
    Form,
  }
}
</script>

<style scoped>

</style>
