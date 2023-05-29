<template>
  <div>
    <h1>Контакты:</h1>
    <div>
      <!-- Telegram -->
      <div
        class="link-container">
        <img
          src="/telegram-svgrepo-com.svg"
          class="image"/>
        <h2>Telegram: @bananadja</h2>
      </div>

      <!-- Email -->
      <div
          class="link-container">
          <img
            src="/gmail-svgrepo-com.svg"
            class="image"/>
          <h2>Email: nadeshda.batova@yandex.ru</h2>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
</script>


<style scoped>
.link-container {
  display: flex;
  color: black;
}

.image {
  margin-right: 5px;
  width: 30px;
}
</style>