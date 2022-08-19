<template>
  <div>
    <v-row dense>
      <v-col cols="12">
        <v-card class="pa-4">
          <template v-slot:prepend>
            <v-avatar size="x-large" color="#224F66">
              <v-icon icon="mdi-vuejs" color="green" size="50" />
            </v-avatar>
          </template>
          <template v-slot:title>
            <span class="text-h5 font-weight-bold">Vue App About</span>
          </template>
          <template v-slot:subtitle> @aprendavue</template>
          <AboutCardItems :items="app" />
        </v-card>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="Autor" :items="author">
          <AboutCardItems :items="author" />
        </v-card>
      </v-col>

      <v-col>
        <v-card title="Empresa">
          <AboutCardItems :items="company" />
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script setup lang="ts">
import { AboutItems } from '../types'
import { ref } from 'vue'
import AboutCardItems from '../components/AboutCardItems.vue'
const author = ref<AboutItems[]>([
  {
    title: 'Beto Garcia',
    subtitle: 'SP - Brasil',
    icon: 'mdi-account'
  },
  {
    title: 'Download From Cloud',
    icon: 'mdi-download'
  }
])
const company = ref<AboutItems[]>([
  {
    title: 'Aprenda Vue',
    subtitle: 'Aprenda Vue',
    icon: 'mdi-domain'
  },
  {
    subtitle: 'Av Brigadeiro Faria Lima, 245, São Paulo - SP',
    icon: 'mdi-map-marker'
  }
])
const app = ref<AboutItems[]>([
  {
    title: 'Versão',
    subtitle: '1.0.6',
    icon: 'mdi-information'
  },
  {
    title: 'Changelog',
    icon: 'mdi-refresh'
  },
  {
    title: 'Licença',
    icon: 'mdi-book-information-variant'
  }
])
</script>

<style scoped></style>
