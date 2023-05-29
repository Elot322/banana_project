<template>
  <div
      class="main-container"
      @click="onCardClick">
      <h3>
        {{ props.text }}
      </h3>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  text: string,
  link: string,
}>()

function onCardClick() {
  window.open(props.link)
}

</script>


<style>
.main-container {
  padding: 20px;
  box-shadow: 2px 2px 2px black;
  border-radius: 25px;
  background-color: rgb(220, 220, 220);
  margin-bottom: 20px;
  cursor: pointer;
  transition-duration: 500ms;
}

.main-container:hover {
  transition-duration: 500ms;
  background-color: #ffc33c;
}
</style>