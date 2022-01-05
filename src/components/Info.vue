<template>
  <div>
    <p v-if="isWorking">I'm working at this moment.</p>
    <p v-else>I'm looking for a job at this moment.</p>
    <p>I use the following technologies for the backend:</p>
    <ul>
      <li v-for="(technology, index) in backend_technologies" :key="index">
        {{ technology }}
      </li>
    </ul>
    <p>I use the following technologies for the frntend:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.ftechnology }}
      </li>
    </ul>
    <p></p>
    <div>
      <button @click="showEmail">{{ buttonText }}</button>
    </div>
    <!-- <p v-if="!isWorking">Send a mail to: {{ email }}</p> -->
    <p v-show="show_email">Send a mail to: {{ email }}</p>
    <p>To access my portfolio 
      <a v-bind:href="portfolio" target="_blank">
      click here
      </a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from './Picture.vue';
export default {
  name: 'Info',
  data() {
    return {      
      show_email: false,
      portfolio: 'https://www.upwork.com/freelancers/~01e098fb79f01796b4',
      buttonText: 'Show Email',
      backend_technologies: ['JavaSript', 'Node.js', 'express'],
      frontend_technologies: [
        {id: 1, ftechnology: 'React-native'},
        {id: 2, ftechnology: 'Vue.js'},
        {id: 3, ftechnology: 'Next.js'},
        {id: 4, ftechnology: 'Nuxt.js'}
      ],
    }
  },
  components: {
    Picture,
  },
  props: {
    email: String,
    isWorking: Boolean
  },
  methods: {
    showEmail() {
      this.show_email = !this.show_email;
      if (!this.show_email) {
        this.buttonText = 'Show email'
      } else {
        this.buttonText = 'Hide email'
      }
    }
  }
}
</script>

<style scoped>
</style>