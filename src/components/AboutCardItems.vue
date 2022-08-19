<script setup lang="ts">
import { AboutItems } from '../types'
interface Props {
  items: AboutItems[]
}
defineProps<Props>()
</script>

<template>
  <v-card-item
    v-for="item in items"
    :key="item.title"
    :title="item.title"
    :subtitle="item.subtitle"
    :prepend-icon="item.icon"
  ></v-card-item>
</template>
