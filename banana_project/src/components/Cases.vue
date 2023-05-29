<template>
  <div>
    <h1>Кейсы:</h1>
      <div
          class="row-cases">
          <CasesCard
              v-for="(card, index) in props.cards" :key="index"
              :link="card.link"
              :text="card.text"
              class="card-container"/>
      </div>
  </div>
</template>

<script setup lang="ts">
import {ref} from "vue";

import CasesCard from "./CasesCard.vue";

const props = defineProps<{
  cards: {
    text: string,
    link: string
  }[]
}>()

</script>

<style scoped>
.row-cases {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.card-container {
  display: inline-block;
  width: 200px;
}
</style>