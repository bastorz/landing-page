<template>
  <div class="flex justify-center p-12" v-editable="blok">

    <form
      :name="blok.name"
      method="POST"
      data-netlify="true"
      :action="`${blok.navigationSuccess.cached_url}`"
      class="flex flex-col w-[400px]"
    >
      <StoryblokComponent
        v-for="form in blok.forms"
        :key="form._uid"
        :blok="form"
      />
      <button
        type="submit"
        class="w-full rounded-[8px] bg-primary px-6 py-2.5 text-xs font-medium uppercase leading-tight text-white shadow-md transition duration-150 ease-in-out bg-[#00b3b0] hover:bg-[#009f9c] hover:shadow-lg focus:bg-[#009f9c] focus:shadow-lg focus:outline-none focus:ring-0 active:bg-[#009f9c] active:shadow-lg"
      >
        Send
      </button>
    </form>
  </div>
</template>
<script setup>
defineProps({ blok: Object });
</script>
