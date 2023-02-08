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
    <img alt="Schneider"
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
</script>

<script>
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

function getRandomColor() {
  var letters = "0123456789ABCDEF";
  var color = "#";
  for (var i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return color;
}

document.querySelector(".buttons").addEventListener("mouseover", function (e) {
  e.target.style.color = "purple";
});

document.querySelector(".buttons").addEventListener("mouseleave", function (e) {
  e.target.style.color = "black";
});

toggleBackground.addEventListener("click", function (e) {
  card.style.backgroundColor = getRandomColor();
  body.style.backgroundColor = getRandomColor();
});

detailButton.addEventListener("click", function (e) {
  var paragraphs = wordsInCard;
  if (paragraphs.style.display === "none") {
    paragraphs.style.display = "block";
  } else {
    paragraphs.style.display = "none";
  }
});

addEventListener("load", function (e) {
  if (title.innerHTML === "Bryce Schneider") {
    title.innerHTML = "Something Else";
  } else {
    title.innerHTML = "Bryce Schneider";
  }
});

changeTitle.addEventListener("click", function (e) {
  if (title.innerHTML === "Bryce Schneider") {
    title.innerHTML = "Something Else";
  } else {
    title.innerHTML = "Bryce Schneider";
  }
});

copyButton.addEventListener("click", function (e) {
  const clone = card.cloneNode(true);
  document.body.appendChild(clone);
  cardCount++;
});

deleteButton.addEventListener("click", function (e) {
  if (cardCount > 1) {
    document.body.removeChild(document.querySelector(".card"));
    cardCount--;
  }
});
// if you are reading this you are very handsome

</script>

<style scoped>
a {
  color: #42b983;
}
</style>
