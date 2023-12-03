<script setup>
const textButton = ref("Pokaż tekst")
const showText = ref(false)

const handleButton = () => {
  textButton.value = !showText.value ? "Ukryj tekst" : "Pokaż tekst";
  // if (!showText.value) {
  //   textButton.value = "Ukryj tekst"
  // } else {
  //   textButton.value = "Pokaż tekst"
  // }
  return showText.value = !showText.value

}
</script>
<template>
    <div>
      <button @click="handleButton">{{ textButton }}</button>
      <h1 v-if="showText">V-if</h1>
      <span v-show="showText">V-show</span>
    </div>
</template>
<style scoped>

</style>