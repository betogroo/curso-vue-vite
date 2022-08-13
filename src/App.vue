<template>
  <v-app>
    <v-navigation-drawer permanent>
      <v-list nav density="compact">
        <v-list-item
          color="primary"
          v-for="item in items"
          :key="item.name"
          :title="item.title"
          :prepend-icon="item.icon"
          :to="{ name: item.name }"
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

<script setup lang="ts">
import { ref } from 'vue'
interface Drawer {
  name: string
  title: string
  icon: string
}

const items = ref<Drawer[]>([
  {
    name: 'HomeView',
    icon: 'mdi-home',
    title: 'Home'
  },
  {
    name: 'AboutView',
    icon: 'mdi-information',
    title: 'About'
  },
  {
    name: 'CounterView',
    icon: 'mdi-counter',
    title: 'Contador'
  }
])
</script>

<style scoped></style>
