<script setup>
const route = useRoute();
const page = ref();
onMounted(() => {
  page.value = route.params.page;
})
</script>

<style>
</style>

<template>
  <NuxtLayout>
    <div v-if="page === 'login'">
      <UserLogin/>
    </div>
    <div v-else-if="page === 'register'">
      <NewUser/>
    </div>
  </NuxtLayout>
</template>