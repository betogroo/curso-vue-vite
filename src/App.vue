<template>
  <v-app>
    <v-navigation-drawer permanent>
      <ul>
        <li>
          <router-link :to="{ name: 'HomeView' }">Home</router-link>
        </li>
        <li>
          <router-link :to="{ name: 'AboutView' }">About</router-link>
        </li>
      </ul>
    </v-navigation-drawer>
    <v-main>
      <v-container>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup lang="ts"></script>

<style scoped></style>
