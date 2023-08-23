<template>
  <div v-editable="blok">
    <StoryblokComponent
      v-for="blok_item in blok.body"
      :key="blok._uid"
      :blok="blok_item"
      class="flex"
    />
  </div>
</template>

<script setup>
const props = defineProps({ blok: Object });
</script>
