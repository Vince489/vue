<template>
  <div>
    <h1>I'm home!</h1><hr>
    <form @submit.prevent="login">
      <label for="gamerTag">login: </label>
      <input type="text" id="gamerTag" name="gamerTag" v-model="gamerTag" placeholder="Gamertag" required>
      <input type="email" id="email" v-model="email" placeholder="Email" required>
      <input type="submit" id="submit" placeholder="submit">
    </form>
    <p>Gamertag: {{ gamerTag }} </p>
    <p>Email: {{ email }} </p>
  </div>
</template>

<script setup>

import { ref } from 'vue'

const gamerTag = ref(null)
const email = ref(null)


const login = () => {
  console.log(gamerTag.value)
  console.log(email.value)
  return (gamerTag.value, email.value)
}



</script>

<style scoped>

</style>