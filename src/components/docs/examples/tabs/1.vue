<template>
  <div>
    <v-tabs dark v-model="active">
      <v-tabs-bar slot="activators">
        <v-tabs-item
          v-for="tab in tabs"
          :key="tab"
          :href="'#' + tab"
          ripple
        >
          Item {{ tab.slice(-1) }}
        </v-tabs-item>
        <v-tabs-slider class="accent"></v-tabs-slider>
      </v-tabs-bar>
      <v-tabs-content v-for="tab in tabs" :key="tab" :id="tab">
        <v-card flat>
          <v-card-text>{{ text }}</v-card-text>
        </v-card>
      </v-tabs-content>
    </v-tabs>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        tabs: ['tab-1', 'tab-2', 'tab-3'],
        active: null,
        text: 'Lorem ipsum dolor sit amet...'
      }
    },
    methods: {
      next () {
        this.active = this.tabs[(this.tabs.indexOf(this.active) + 1) % this.tabs.length]
      }
    }
  }
</script>
