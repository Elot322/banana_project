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
      <div class="photo"></div>
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
    height: 150px;
    width: 150px;
    background-color: red;
    background-image: url('/photo.JPG');
    background-size: cover;
  }
</style>