<script>
export default {
  name: 'HelloWorldOptionsApi',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0,
      msgAlt: "Mon second message"
    }
  },
  methods: {
    incrementCount() {
      this.count++
      this.$emit('counterUpdated')
    }
  }
}
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <div>Mon compteur: {{ count }}<button @click="incrementCount">+</button></div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
