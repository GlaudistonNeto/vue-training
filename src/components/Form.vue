<template>
  <form action="" @submit="sendForm($event)">
    <div>
      <input type="text" v-model="name" placeholder="Name">
    </div>
    <div>
      <input type="text" v-model="email" placeholder="Email">
    </div>
    <div>
      <Submit />
    </div>
    <div class="reuse">
      <TheReuse />
    </div>
  </form>
  <p>Content</p>
  <p>Content</p>
  <p>Content</p>
</template>

<script>
import InputText from './form/InputText.vue';
import Submit from './form/Submit.vue';
import TheReuse from './TheReuse.vue';
export default {
  name: 'Form',
  components: {
    InputText,
    Submit,
    TheReuse,
  },
  data() {
    return {
      name: '',
      email: '',
    }
  },
  methods: {
    sendForm(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log('Your name is : ' + name);
      console.log('And your email is : ' + email);
    }
  }
}
</script>

<style scoped>
  p {
    margin: 50px;
  }
  .reuse {
    margin-top: 10px;
  }
</style>
