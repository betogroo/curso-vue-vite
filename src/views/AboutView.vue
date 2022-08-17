<template>
  <div>
    <v-row dense>
      <v-col cols="12">
        <v-card>
          <template v-slot:prepend>
            <v-avatar size="x-large" color="yellow">
              <span class="text-h3">JS</span>
            </v-avatar>
          </template>
          <template v-slot:title>
            <span class="text-h4">Vue App About</span>
          </template>
          <template v-slot:subtitle> @jsprogramers</template>
          <v-card-item
            title="Versão"
            subtitle="1.0.6"
            prepend-icon="mdi-information"
          ></v-card-item>
          <v-card-item
            title="Changelog"
            prepend-icon="mdi-refresh"
          ></v-card-item>
          <v-card-item
            title="Licença"
            prepend-icon="mdi-book-information-variant"
          ></v-card-item>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6">
        <v-card>
          <v-card-title>Autor</v-card-title>
          <v-card-item
            title="Beto Garcia"
            subtitle="São Paulo - Brasil"
            prepend-icon="mdi-account"
          ></v-card-item>
          <v-card-item
            title="Download"
            prepend-icon="mdi-download"
          ></v-card-item>
        </v-card>
      </v-col>
      <v-col>
        <v-card>
          <v-card-title>Empresa</v-card-title>
          <v-card-item
            subtitle="Especialistas em Javascript"
            title="JS Programers "
            prepend-icon="mdi-domain"
          ></v-card-item>
          <v-card-item
            subtitle="Av Brigadeiro Faria Lima, 245 - São Paulo SP "
            prepend-icon="mdi-map-marker"
          ></v-card-item>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
