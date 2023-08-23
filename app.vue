<template>
  <div >
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
<script setup>
import { initFlowbite } from "flowbite";
onMounted(() => {
  initFlowbite();
});
</script>
