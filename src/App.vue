<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello World! (Bryce Schneider was here hehe)" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background: grey;
}

.card {
  width: 300px;
  text-align: center;
  border: 3px solid yellow;
  margin-top: 40px;
  margin-bottom: 40px;
  margin-right: 40px;
  margin-left: 80px;
  padding-bottom: 16px;
  padding-right: 8px;
  padding-left: 8px;
  box-shadow: 3px 3px;
  border-radius: 25px;
  background: blue;
}

.paragraph {
  font-size: 18px;
  color: white;
  margin-top: 24px;
  margin-bottom: 24px;
  margin-right: 24px;
  margin-left: 24px;
}

.header {
  font: 38px Papyrus;
  color: white;
  margin-bottom: 16px;
}

.buttons button {
  border-radius: 25px;
}

.details {
  border-radius: 25px;
  color: yellow;
  background-color: #4caf50;
}

button:hover,
button:focus {
  background-color: yellow;
}

.image {
  border: 3px solid yellow;
}

@media (max-width: 800px) and (min-width: 500px) {
  .button {
    display: none;
  }
}

@media (max-width: 500px) {
  * {
    transform: scale(0.8);
  }
}
</style>
