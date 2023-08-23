<template>
  <div class="bg-black"> <StoryblokComponent v-if="story" :blok="story.content" /></div>
</template>

<script setup>
const story = await useAsyncStoryblok("home", {
    version: "draft",
    language: "es",
  });
</script>

