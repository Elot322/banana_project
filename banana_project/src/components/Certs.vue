<template>
  <div>
    <h1>Сертификаты:</h1>
    <div
        v-for="(card, index) in props.cards" :key="index"
        class="container">
        <CertCard
            :link="card.link"
            :text="card.text"
            class="card-container"/>
    </div>
  </div>
</template>

<script setup lang="ts">

import CertCard from "./CertCard.vue";

const props = defineProps<{
  cards: {
    text: string,
    link: string
  }[]
}>()

</script>

<style>
.container {
  align-items: center;
}

.card-container {
  text-align: center;
  margin-left: auto;
  margin-right: auto;
}
</style>