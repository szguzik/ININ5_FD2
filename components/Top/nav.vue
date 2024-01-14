<script setup>
const props = defineProps({
  itemsMenu: {
    type: Array,
    default: () => []
    // required: true
  }
})

onMounted(() => {
  console.log(props.itemsMenu);
})
</script>

<template>
  <div class="navbar navbar-expand-lg bg-light navbar-light">
    <div class="container-fluid">
      <a href="index.html" class="navbar-brand">Burger <span>King</span></a>
      <button type="button" class="navbar-toggler" data-toggle="collapse" data-target="#navbarCollapse">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse justify-content-between" id="navbarCollapse">
        <div class="navbar-nav ml-auto">
          <NuxtLink v-for="item of itemsMenu" :to="item.to" class="nav-item nav-link">{{ item.name }}</NuxtLink>
        </div>
      </div>
    </div>
  </div>
  <!-- Nav Bar End -->
</template>