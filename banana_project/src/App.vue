<template>
  <div>
    <div class="content">
      <div class="content_block">
        <AboutMe/>
      </div>
      <Sticker/>
      <div class="content_block">
        <WorkStyle/>
      </div>
      <div class="content_block">
        <Cases
          :cards="cardsCase"/>
      </div>
      <div class="content_block">
        <Certs
            :cards="cardsCerts"/>
      </div>

        <Contacts/>

    </div>
  </div>
</template>

<script setup lang="ts">
import {ref} from "vue";

import AboutMe from "./components/AboutMe.vue";
import Sticker from "./components/Sticker.vue";
import WorkStyle from "./components/WorkStyle.vue";
import Cases from "./components/Cases.vue";
import Certs from "./components/Certs.vue";
import Contacts from "./components/Contacts.vue";

const cardsCase = ref<{link: string, text: string,}[]>([
  {
    link: '/content.pdf',
    text: 'CONTENT'
  },
 {
    link: 'designs.pdf',
    text: 'DESIGNS'
  },
  {
    link: '/events.pdf',
    text: 'EVENTS'
  },
])

const cardsCerts = ref<{link: string, text: string,}[]>([
  {
    link: '/fin.pdf',
    text: 'Калужский филиал ФГО БУ ВО Финансовый университет при Правительстве РФ'
  },
  {
    link: '/mgeu.pdf',
    text: 'Московский гуманитарно-экономический университет, Калужский институт'
  },
  {
    link: '/featuretoday.pdf',
    text: 'Future Today'
  },
  {
    link: '/canva.pdf',
    text: 'Canva'
  },
])

</script>

<style scoped>
  .content {
    padding-top: 20px;
    padding-bottom: 20px;
    padding-left: 30px;
    padding-right: 30px;
  }

  .content_block {
    padding: 20px;
    box-shadow: 2px 2px 2px rgba(255, 69, 0, 0.45);
    border-radius: 25px;
    background-color: rgba(255, 255, 255, 85%);
    margin-bottom: 20px;
  }
</style>
