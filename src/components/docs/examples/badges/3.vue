<template>
  <div class="text-xs-center">
    <span v-badge:1.left>Primary</span>
    <span v-badge:list.icon class="accent--after">Accent</span>
    <span v-badge:3 class="secondary--after">Secondary</span>
  </div>
</template>

<style scoped>
  span {
    margin: 0 16px;
    line-height: 16px;
  }

  div {
    margin: 14px;
  }
</style>
