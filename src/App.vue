<template>
  <v-app light>
    <v-toolbar fixed>
      <v-toolbar-title v-text="title"></v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon v-for="(theme, index) in themes" :key="index">
        <theme-icon :colors="theme"></theme-icon>
      </v-btn>
    </v-toolbar>
    <main>
      <v-container fluid>
        <v-layout column align-center>
        </v-layout>
      </v-container>
    </main>
  </v-app>
</template>

<script>
  const ThemeIcon = () => import('./components/ThemeIcon.vue')

  export default {
    components: {'theme-icon': ThemeIcon},
    data () {
      return {
        title: 'Vuetify Dynamic Themes',
        themes: [
          ['teal', 'orange', 'grey'],
          ['pink', 'indigo', 'grey'],
          ['indigo', 'purple', 'pink'],
          ['orange', 'red', 'grey'],
          ['grey', 'blue', 'orange'],
          ['black', 'grey', 'green']
        ]
      }
    }
  }
</script>

<style lang="stylus">
  @import './stylus/main'
</style>
