<template>
  <svg height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg">
    <path :fill="colors[0]" d="M 11.000001,1.0544635 A 11,11 0 0 0 1,11.999782 11,11 0 0 0 11.000001,22.949 Z"/>
    <path :fill="colors[1]" d="m 13.000001,1.0505635 v 9.9492185 h 9.945311 A 11,11 0 0 0 13.000001,1.0505635 Z"/>
    <path :fill="colors[2]" d="m 13.000001,12.999776 v 9.945312 a 11,11 0 0 0 9.949217,-9.945312 z"/>
  </svg>
</template>

<script>
export default {
  name: 'theme-icon',
  props: ['colors']
}
</script>
