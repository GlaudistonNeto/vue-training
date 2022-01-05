<template>
  <div>
    <button
      @click="first(txt1, $event),
              second(txt2, $event),
              third()"
    >
      Activate Multiple Events
    </button>
    <p>{{ multiple_events }}</p>
  </div>
</template>

<script>
export default {
  name: 'MultipleEvents',
  data() {
    return {
      multiple_events: '',
      txt1: 'First event activated!',
      txt2: 'Second event activated!'
    }
  },
  methods: {
    first(txt, e) {
      this.multiple_events = txt;
    },
    second(txt, e) {
      setTimeout(() => 
        this.multiple_events = txt, 1500
      );
    },
    third() {
      setTimeout(() => 
        this.multiple_events = "", 3000
      );
    },
  }
}
</script>

<style scoped>
  div {
    margin: 100px;
  }
</style>
