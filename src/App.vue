<script setup lang="ts">
import { ref } from 'vue'

interface DrawerItems {
  name: string
  title: string
  icon: string
}

const drawer = ref<boolean>(true)

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
  <v-app class="bg-indigo-lighten-5">
    <v-navigation-drawer v-model="drawer">
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
    <v-app-bar density="compact">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title> Vue App </v-app-bar-title>
      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<style scoped></style>
