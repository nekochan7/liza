<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>{{ name }}</h1>
  </div>
</template>

<script>

export default {
  name: 'Home',

  data: () => ({
    name: process.env.VUE_APP_NAME
  })
}
</script>
