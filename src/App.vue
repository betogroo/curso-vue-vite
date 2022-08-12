<template>
  <v-app>
    <v-navigation-drawer permanent>
      <v-list nav density="compact">
        <v-list-item
          title="Home"
          prepend-icon="mdi-home"
          :to="{ name: 'HomeView' }"
        />
        <v-list-item
          title="About"
          prepend-icon="mdi-information"
          prefix="Coiso"
          :to="{ name: 'AboutView' }"
        />
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
