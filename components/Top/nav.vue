<script setup>
const obj = ref(null)
const title = ref("")
const props = defineProps({
  itemsMenu: {
    type: Array,
    default: () => []
    // required: true
  }
})
async function logData() {
  const response = await fetch("https://jsonplaceholder.typicode.com/todos/1");
  obj.value = await response.json();
  title.value = obj.value ? " - " + obj.value.title : "";
  console.log(obj.value.title);
}

onMounted(() => {
  console.log(props.itemsMenu);

  logData();
})
</script>

<template>
  <div class="navbar navbar-expand-lg bg-light navbar-light">
    <div class="container-fluid">
      <a href="index.html" class="navbar-brand">Burger <span>King{{ title }}</span></a>
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