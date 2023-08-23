<template>
  <div class="form-group mb-6 flex">
    <input
      type="checkbox"
      :name="blok.name"
      class="mr-4"
      :id="blok.name"
      :required="blok.required"
    />
    <label :for="blok.name">{{ blok.label }}</label>
  </div>
</template>
<script setup>
defineProps({ blok: Object });
</script>
