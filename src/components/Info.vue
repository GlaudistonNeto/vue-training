<template>
  <div>
    <p v-if="isWorking">I'm working at this moment.</p>
    <p v-else>I'm looking for a job at this moment.</p>
    <p>I use the following technologies:</p>
    <ul>
      <li>JavaSript</li>
      <li>Node.js</li>
      <li>Vue.js</li>
      <li>React-native</li>
    </ul>
    <!-- <p v-if="!isWorking">Send a mail to: {{ email }}</p> -->
    <p v-show="showEmail">Send a mail to: {{ email }}</p>
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
      isWorking: false,
      showEmail: true,
      email: 'glaudistonson@gmail.com',
      portfolio: 'https://www.upwork.com/freelancers/~01e098fb79f01796b4'
    }
  },
  components: {
    Picture,
  }
}
</script>

<style scoped>

</style>
