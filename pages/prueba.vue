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
     <div class="w-full flex items-center justify-center bg-gradient-to-r from-purple-900 to-pink-700  h-screen py-60">
        <form 
        name="contactus" 
        action="/prueba" 
        method="post" 
        data-netlify="true"
        
        >
            <input type="hidden" name="form-name" value="contactus" />
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
     </div>
    
       <!-- <StoryblokComponent v-if="story" :blok="story.content" /> -->

</template>

    <script setup>
    import { defineComponent, h } from 'vue'
    import {
      ArrowPathIcon,
      ChevronRightIcon,
      CloudArrowUpIcon,
      Cog6ToothIcon,
      FingerPrintIcon,
      LockClosedIcon,
      ServerIcon,
    } from '@heroicons/vue/20/solid'
    import { BoltIcon, CalendarDaysIcon, UsersIcon } from '@heroicons/vue/24/outline'
    
    const primaryFeatures = [
      {
        name: 'Server monitoring',
        description:
          'Non quo aperiam repellendus quas est est. Eos aut dolore aut ut sit nesciunt. Ex tempora quia. Sit nobis consequatur dolores incidunt.',
        href: '#',
        icon: BoltIcon,
      },
      {
        name: 'Collaborate',
        description:
          'Vero eum voluptatem aliquid nostrum voluptatem. Vitae esse natus. Earum nihil deserunt eos quasi cupiditate. A inventore et molestiae natus.',
        href: '#',
        icon: UsersIcon,
      },
      {
        name: 'Task scheduling',
        description:
          'Et quod quaerat dolorem quaerat architecto aliquam accusantium. Ex adipisci et doloremque autem quia quam. Quis eos molestiae at iure impedit.',
        href: '#',
        icon: CalendarDaysIcon,
      },
    ]
    const secondaryFeatures = [
      {
        name: 'Push to deploy.',
        description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit aute id magna.',
        icon: CloudArrowUpIcon,
      },
      {
        name: 'SSL certificates.',
        description: 'Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo.',
        icon: LockClosedIcon,
      },
      {
        name: 'Simple queues.',
        description: 'Ac tincidunt sapien vehicula erat auctor pellentesque rhoncus.',
        icon: ArrowPathIcon,
      },
      {
        name: 'Advanced security.',
        description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit aute id magna.',
        icon: FingerPrintIcon,
      },
      {
        name: 'Powerful API.',
        description: 'Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo.',
        icon: Cog6ToothIcon,
      },
      {
        name: 'Database backups.',
        description: 'Ac tincidunt sapien vehicula erat auctor pellentesque rhoncus. ',
        icon: ServerIcon,
      },
    ]
    const stats = [
      { id: 1, name: 'Developers on the platform', value: '8,000+' },
      { id: 2, name: 'Daily requests', value: '900m+' },
      { id: 3, name: 'Uptime guarantee', value: '99.9%' },
      { id: 4, name: 'Projects deployed', value: '12m' },
    ]
    const footerNavigation = {
      solutions: [
        { name: 'Hosting', href: '#' },
        { name: 'Data Services', href: '#' },
        { name: 'Uptime Monitoring', href: '#' },
        { name: 'Enterprise Services', href: '#' },
      ],
      support: [
        { name: 'Pricing', href: '#' },
        { name: 'Documentation', href: '#' },
        { name: 'Guides', href: '#' },
        { name: 'API Reference', href: '#' },
      ],
      company: [
        { name: 'About', href: '#' },
        { name: 'Blog', href: '#' },
        { name: 'Jobs', href: '#' },
        { name: 'Press', href: '#' },
        { name: 'Partners', href: '#' },
      ],
      legal: [
        { name: 'Claim', href: '#' },
        { name: 'Privacy', href: '#' },
        { name: 'Terms', href: '#' },
      ],
      social: [
        {
          name: 'Facebook',
          href: '#',
          icon: defineComponent({
            render: () =>
              h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
                h('path', {
                  'fill-rule': 'evenodd',
                  d: 'M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z',
                  'clip-rule': 'evenodd',
                }),
              ]),
          }),
        },
        {
          name: 'Instagram',
          href: '#',
          icon: defineComponent({
            render: () =>
              h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
                h('path', {
                  'fill-rule': 'evenodd',
                  d: 'M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z',
                  'clip-rule': 'evenodd',
                }),
              ]),
          }),
        },
        {
          name: 'Twitter',
          href: '#',
          icon: defineComponent({
            render: () =>
              h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
                h('path', {
                  d: 'M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84',
                }),
              ]),
          }),
        },
        {
          name: 'GitHub',
          href: '#',
          icon: defineComponent({
            render: () =>
              h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
                h('path', {
                  'fill-rule': 'evenodd',
                  d: 'M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z',
                  'clip-rule': 'evenodd',
                }),
              ]),
          }),
        },
        {
          name: 'YouTube',
          href: '#',
          icon: defineComponent({
            render: () =>
              h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
                h('path', {
                  'fill-rule': 'evenodd',
                  d: 'M19.812 5.418c.861.23 1.538.907 1.768 1.768C21.998 8.746 22 12 22 12s0 3.255-.418 4.814a2.504 2.504 0 0 1-1.768 1.768c-1.56.419-7.814.419-7.814.419s-6.255 0-7.814-.419a2.505 2.505 0 0 1-1.768-1.768C2 15.255 2 12 2 12s0-3.255.417-4.814a2.507 2.507 0 0 1 1.768-1.768C5.744 5 11.998 5 11.998 5s6.255 0 7.814.418ZM15.194 12 10 15V9l5.194 3Z',
                  'clip-rule': 'evenodd',
                }),
              ]),
          }),
        },
      ],
    }
    
    const story = await useAsyncStoryblok("prueba", {
    version: "draft",
    language: "es",
  });
    </script>
    
    