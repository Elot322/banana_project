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

import CasesCard from "./CasesCard.vue";

const props = defineProps<{
  cards: {
    text: string,
    link: string
  }[]
}>()

</script>

<style scoped>
@media (min-width:1200px) {
  .row-cases {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .card-container {
    display: inline-block;
    width: 200px;
  }
}
@media screen and (min-width: 320px) and (max-width: 480px){
  .row-cases {
    display: block;
    justify-content: space-between;
  }
  .card-container {
    text-align: center;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>