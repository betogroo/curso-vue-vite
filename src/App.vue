<script setup lang="ts">
import { ref } from 'vue'

interface DrawerItems {
  name: string
  title: string
  icon: string
}

const items = ref<DrawerItems[]>([
  {
    name: 'HomeView',
    icon: 'mdi-home',
    title: 'Home'
  },
  {
    name: 'CounterView',
    icon: 'mdi-counter',
    title: 'Counter'
  },
  {
    name: 'AboutView',
    icon: 'mdi-information',
    title: 'About'
  }
])
</script>
<template>
  <v-app>
    <v-navigation-drawer permanent>
      <v-list nav density="compact">
        <v-list-item
          v-for="item in items"
          :key="item.name"
          :prepend-icon="item.icon"
          :title="item.title"
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

<style scoped></style>
