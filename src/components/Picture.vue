<template>
  <img class="container" :src="avatar" :alt="description">
</template>

<script>
export default {
  name: 'Picture',
  data() {
    return {
      avatar: "/img/avatar.png",
      description: "G-Neto"
    }
  }
}
</script>

<style scoped>
  .container {
    margin-left: 25px;
  }
</style>
