<template>
  <div class="buttons">
    <button class="copy" v-on:click="duplicate">Duplicate</button>
    <button class="changeBackground" v-on:click="background">Change Background</button>
    <button class="changeTitle" v-on:click="title">Change Title</button>
    <button id="delete" v-on:click="delete">Delete
      Last Instance</button>
  </div>
  <div class="card">
    <h2 class="header">
      Bryce Schneider
    </h2>
    <img class="image" alt="Schneider"
      src="https://cdn.discordapp.com/attachments/1062806966021402684/1063160172773654659/IMG_9420.png" />
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
const card = document.querySelector(".card");
</script>

<script>

export default {

  methods: {

    getRandomColor() {
      var letters = "0123456789ABCDEF";
      var color = "#";
      for (var i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }
      return color;
    },

    duplicate() {
      const toggleBackground = document.querySelector(".changeBackground");

      const changeTitle = document.querySelector(".changeTitle");

      const deleteButton = document.querySelector("#delete");

      const copyButton = document.querySelector(".copy");

      const card = document.querySelector(".card");

      const wordsInCard = document.querySelector("p");

      const body = document.querySelector("body");

      const detailButton = document.querySelector(".details");

      var cardCount = 1;

      var title = document.querySelector(".header");

      const clone = card.cloneNode(true);
      document.body.appendChild(clone);
    },

    background() {
      card.style.backgroundColor = getRandomColor();
      body.style.backgroundColor = getRandomColor();
    },

    title() {

    },

    delete() {
      document.body.removeChild(document.querySelector(".card:last-child"));
    },

  }
}


</script>

<style scoped>
a {
  color: #42b983;
}
</style>
