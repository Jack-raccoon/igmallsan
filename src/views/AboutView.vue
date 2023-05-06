<script setup>
import  footerComponent  from './../components/footerComponent.vue'
</script>

<template>
  <div class=" view about">
    <h1>This is an about page</h1>
  </div>
  <footerComponent />
</template>

<style>

.about {
  min-height: 100vh;
  display: flex;
  align-items: center;
}

@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
