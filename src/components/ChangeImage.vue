<template>
  <div>
    <button id="mp" @click="$emit('changeImage')">Change Profile Image</button>
  </div>
</template>

<script>
export default {
  name: 'ChangeImage',
  emits: ['changeImage']
}
</script>

<style scoped>
  #mp {
    margin-bottom: 10px;
  }
</style>
