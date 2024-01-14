<script setup>
const menu = [
  {
    "name": "Home",
    "to":  "/"
  },
  {
    "name": "About (SPA)",
    "to":  "/about"
  }
]

</script>

<template>
  <div>
      <TopNav :itemsMenu="menu"/>
      <NuxtPage/>
  </div>
</template>
