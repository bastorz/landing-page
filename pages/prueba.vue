<template>
        <!-- <form
          :name="blok.name"
          method="POST"
          netlify
          :action="`${blok.navigationSuccess.cached_url}`"
          class="flex flex-col w-[400px]  pt-10"
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
        </form> -->
     <!-- <div class="w-full flex items-center justify-center bg-gradient-to-r from-purple-900 to-pink-700 h-screen py-60">
        <form 
        name="contactForm" action="/" method="post" data-netlify="true"
        >
            <input type="hidden" name="contactForm" value="contactForm" />
            <div class="flex items-center justify-center flex-col text-white text-4xl space-y-4 py-4">  
                <label for="name">Name:</label> 
                <input type="text" name="name" required/>
            </div>
            <div class="flex items-center justify-center flex-col text-white text-4xl space-y-4 py-4">
                <label for="email">Email:</label>
                <input type="email" name="email" required/>
            </div>
            <div class="flex items-center justify-center flex-col text-white text-4xl space-y-4 py-4">
                <label for="message">Message:</label>
                <textarea name="message" required></textarea>
                <button type="submit" value="Send message" class="bg-gradient-to-r from-blue-900 to-blue-500 py-4 px-10 rounded-lg">Send</button>
            </div>
        </form>
     </div> -->
    
       <!-- <StoryblokComponent v-if="story" :blok="story.content" /> -->

</template>

    <script setup>

    const story = await useAsyncStoryblok("prueba", {
    version: "draft",
    language: "es",
  });
    </script>
    
    