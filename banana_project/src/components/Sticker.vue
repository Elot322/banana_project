<template>
  <div class="about">
    <img src="/sticker.png"/>
    <div class="text">
      <h3>{{ typedText }}</h3>
    </div>
  </div>
</template>

<script setup lang="ts">
import {onMounted, ref} from "vue";

let i = 0
const text = 'Приветствую! Меня зовут Надя и это мое портфолио. Ниже можно ознакомиться с проектами над которыми я работала!'

const typedText = ref('')
const speed = 50;

function typeText() {
  if(i < text.length) {
    typedText.value += text.charAt(i)
    i++
    setTimeout(typeText, speed);
  }
}

onMounted(()=>{
  typeText()
})
</script>

<style>
  .about{
    display: flex;
    justify-content: center;
  }
  .text {
    align-items: center;
    width: 300px;
    height: 300px;
  }
  @media (min-width:320px) {
    .text {
      display: none;
    }
  }

</style>