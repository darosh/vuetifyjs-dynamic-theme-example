<template>
  <v-container fluid grid-list-lg>
    <v-layout row wrap>
      <v-flex xs6>
        <v-card>
          <v-card-title primary-title>
            <div class="headline">Normal</div>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs6>
        <v-card class="primary">
          <v-card-title primary-title>
            <div class="headline">Primary</div>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs6>
        <v-card class="secondary">
          <v-card-title primary-title>
            <div class="headline">Secondary</div>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs6>
        <v-card class="accent">
          <v-card-title primary-title>
            <div class="headline">Accent</div>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>
