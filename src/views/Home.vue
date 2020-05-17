<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>{{ name }}</h1>
    <h1>Number : {{ number }}</h1>
    <h1>Fullname : {{ fullName }}</h1>
    <button @click="doIncrement()">increment number</button>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Home',

  data: () => ({
    name: process.env.VUE_APP_NAME,
    fisrtName: 'Ro',
    lastName: 'Ri'
  }),

  computed: {
    fullName () {
      return `${this.fisrtName}${this.lastName}`
    },

    ...mapGetters(['number'])
  },

  methods: {
    doIncrement () {
      this.$store.commit('INCREMENT')
    }
  }
}
</script>
