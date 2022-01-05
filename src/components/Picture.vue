<template>
  <img class="container" :src="avatar" :alt="description">
  <change-image @change-image="changeImage" />
</template>

<script>
import ChangeImage from './ChangeImage.vue';

export default {
  name: 'Picture',
  data() {
    return {
      avatar: "/img/avatar.png",
      description: "G-Neto"
    }
  },
  components: {
    ChangeImage
  },
  methods: {
    changeImage() {
      this.avatar = "/img/avatar2.png";
    }
  }
}
</script>

<style scoped>
  .container {
    margin-left: 15px;
  }
</style>
