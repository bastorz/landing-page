<template>
  <form
    v-editable="blok"
    enctype="multipart/form-data"
    method="post"
    :action="blok.submit"
  >
    <StoryblokComponent
      v-for="blok_item in blok.rows"
      :key="blok_item._uid"
      :blok="blok_item"
      class="mx-auto -mb-7 justify-self-center"
    />
    <div class="w-full flex justify-center">
      <StoryblokComponent
      v-for='blok_item in blok.buttons'
      :key='blok_item._uid'
      :blok='blok_item' 
      class="mx-1"
      />
    </div>
  </form>
</template>
<script setup>
defineProps({ blok: Object });
</script>
<style scoped></style>
