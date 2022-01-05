<template>
  <div>
    <button @click="activate">Click me</button>
    <span v-show="activated">Activated!</span>
  </div>
</template>

<script>
export default {
  name: 'TheReuse',
  methods: {
    activate() {
      this.activated = !this.activated
    }
  },
  data() {
    return {
      activated: false
    }
  }
}
</script>
