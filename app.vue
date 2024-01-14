<script setup>
const menu = [
  {
    "name": "Home",
    "to":  "/"
  },
  {
    "name": "Feature",
    "to":  "/feature"
  },
  {
    "name": "Chef",
    "to":  "/team"
  },
  {
    "name": "Menu",
    "to":  "/menu"
  },
  {
    "name": "Booking",
    "to":  "/booking"
  }
]

</script>

<template>
      <TopNav :items-menu="menu"/>
      <NuxtPage/>
      <Footer/>
</template>
