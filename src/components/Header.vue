<template>
  <ul>
    <li><a href="#" target="_blank">Home</a></li>
    <li><a href="#" target="_blank">Projects</a></li>
    <li><a href="#" target="_blank">Contact</a></li>
  </ul>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped>
  ul {
    list-style: none;
    display: flex;
    background: rgb(99, 99, 99);
  }

  li {
    margin-right: 10px;
  }

  a {
    color: #ddd;
    text-decoration: none;
    transition: 0.5s;
  }

  a:hover {
    color: turquoise;
  }
</style>
