<template>
  <svg height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg">
    <path :fill="colors[0]" d="M 11,0.046875 A 12,12 0 0 0 0,12 12,12 0 0 0 11,23.949219 Z"/>
    <path :fill="colors[1]" d="M 13,0.05078125 V 10.892578 H 23.939453 A 12,12 0 0 0 13,0.05078125 Z"/>
    <path :fill="colors[2]" d="M 13,12.892578 V 23.953125 A 12,12 0 0 0 23.955078,12.892578 Z"/>
  </svg>
</template>

<script>
export default {
  name: 'theme-icon',
  props: ['colors']
}
</script>
