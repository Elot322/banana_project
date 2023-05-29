<template>
  <div class="about">
      <div class="name">
        <h1>
          Батова Надежда
        </h1>
        <h2>
          Маркетинг & PR
        </h2>
      </div>
      <img
          src="/photo.JPG"
          alt="Надежда Батова"
          width="150"
          height="150"
          class="photo"/>
  </div>
</template>

<script setup lang="ts">
</script>

<style>
  .about{
    display: flex;
    justify-content: center;
  }
  .name{
    margin-right: 50px;
    text-align: center;
  }
  .photo{
    border-radius: 100%;
  }
</style>