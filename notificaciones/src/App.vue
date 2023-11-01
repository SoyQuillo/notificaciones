<script setup>
import { ref } from 'vue'
let notifications = ref(0)

function addValue() {
  notifications.value++
}

function restValue() {
  if (notifications.value >= 1) {
    notifications.value--
  }
}
</script>

<template>
  <div class="wrapper">
    <div class="profile-user">
      <div class="notification-user" v-if="notifications > 0">{{ notifications }}</div>
    </div>

    <div class="button-wrapper">
      <div class="button" v-on:click="restValue">-</div>
      <div class="button" v-on:click="addValue">+</div>
    </div>
    <div v-if="notifications == 0">FANTASMA COMO HETOR RIANHO 🤣😂😂🤣🤣😂</div>
    <div v-else="">REVISA TU INBOX 👌👌</div>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: #bdc6cc;
  width: 60%;
  border-radius: 8px;
  margin: 0 auto;
  padding-top: 32px;
  overflow: hidden;
}

.profile-user {
  background-color: purple;
  width: 120px;
  height: 120px;
  margin: auto;
  border-radius: 100%;
  position: relative;
  background-image: url(https://media.licdn.com/dms/image/D4E03AQEUqS-u1-15fw/profile-displayphoto-shrink_800_800/0/1686350648278?e=2147483647&v=beta&t=LgLGai6gbQVy80ivXcuUoELcCtx9ihCq9Xb9ItREDuo);
  background-size: cover;
}

.notification-user {
  position: absolute;
  background-color: red;
  min-width: 18px;
  height: 18px;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  top: 0;
  right: 0;
}

.button-wrapper {
  text-align: center;
  margin: 12px;
}

.button {
  background-color: #04bfad;
  border-radius: 4px;
  padding: 2px 0px;
  font-weight: bold;
  color: white;
  display: inline-block;
  cursor: pointer;
  width: 40px;
}

.button:first-child {
  margin-right: 8px;
}

.button:last-child {
  margin-left: 8px;
}
</style>
