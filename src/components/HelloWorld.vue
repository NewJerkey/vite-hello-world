<template>
  <div class="buttons">
    <button class="copy">Duplicate</button>
    <button class="changeBackground">Change Background</button>
    <button class="changeTitle">Change Title</button>
    <button id="delete">Delete
      Last Instance</button>
  </div>
  <div class="card">
    <h2 class="header">
      Bryce Schneider
    </h2>
    <img alt="Schneider" src="https://cdn.discordapp.com/attachments/1062806966021402684/1063160172773654659/IMG_9420.png" />
    <p class="paragraph">
      This image depicts a strapping young Penn State student reacting to an insane moment in his favorite class: IST
      256. He can not believe what he is seeing!
    </p>
    <button class="details">
      Details
    </button>
  </div>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
