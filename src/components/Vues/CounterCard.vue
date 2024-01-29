<script setup lang="ts">
import { ref } from 'vue'

const scoreRef = ref(100)

const mainTitle = 'Counter in Vue! Can you view it?'
const otherTitle = 'YES'

const title = ref(mainTitle)

function toggleTitle() {
  let titleValue = title.value

  titleValue == mainTitle
    ? (title.value = otherTitle)
    : titleValue == otherTitle
      ? (title.value = mainTitle)
      : ''
  // mainTitle == 'Counter in Vue! Can you view it?'
  //   ? (title.value = otherTitle)
  //   : mainTitle == otherTitle
  //     ? (title.value = mainTitle)
  //     : ''
}
</script>

<template>
  <main>
    <section>
      <!-- <h2 @click="title = 'YES!'">{{ title }}</h2> -->
      <h2 @click="toggleTitle">{{ title }}</h2>
      <h3 class="score">
        Score:
        <span>{{ scoreRef }}</span>
      </h3>
    </section>
    <section class="buttons">
      <button @click="scoreRef++">
        <span>Add <br />+ </span>
      </button>
      <button @click="scoreRef--">
        <span
          >Sub <br />
          -
        </span>
      </button>
    </section>
  </main>
</template>

<style scoped>
main {
  width: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h2 {
  cursor: pointer;
}
.score {
  font-size: 2rem;
  padding-top: 2rem;
}

.buttons {
  padding-top: 2rem;
  display: flex;
  gap: 1.5rem;
}

.buttons button {
  width: 100px;
  height: 100px;
  background-color: antiquewhite;
  font-size: 2rem;
  cursor: pointer;
  text-transform: capitalize;
}
</style>
