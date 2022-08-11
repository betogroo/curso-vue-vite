<template>
  <div>
    <div class="text-center">
      <router-link :to="{ name: 'HomeView' }">Home</router-link> |
      <router-link :to="{ name: 'AboutView' }">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
