<template>
    <div class="counter">
        <p>{{ count }}</p>
        <button @click='increment' >Increment</button>
        <button @click='decrement' >Decrement</button>
    </div>
</template>

<script>
  export default {
    name: 'counter',
    computed: {
      count () {
        return this.$store.state.count
      }
    },
    methods: {
      increment () {
        this.$store.commit('increment')
      },
      decrement () {
        this.$store.commit('decrement')
      }
    }
  }
</script>
