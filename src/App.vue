<template>
  <v-app>
    <v-navigation-drawer permanent>
      <v-list>
        <v-list-item :to="{ name: 'HomeView' }"> Home </v-list-item>
        <v-list-item :to="{ name: 'AboutView' }"> About </v-list-item>
      </v-list>
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
