<template>
  <v-app>
    <div class="text-center">
      <router-link :to="{ name: 'HomeView' }">Home</router-link> |
      <router-link :to="{ name: 'AboutView' }">About</router-link>
    </div>
    <v-main>
      <v-container>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup lang="ts"></script>

<style scoped></style>
