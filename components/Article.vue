<template>
  <div class="py-8 flex flex-wrap md:flex-nowrap">
    <div class="md:flex-grow">
      <h2 class="text-xl font-medium text-gray-900 title-font">
        {{ title }}
      </h2>
      <time class="text-gray-500 text-sm">{{ createdAt }}</time>
      <div class="leading-relaxed pt-4">
        <p>
          {{ description }}
        </p>
        <nuxt-link
          :to="slug"
          class="
            text-yellow-500
            hover:text-yellow-600
            inline-flex
            items-center
            mt-4
          "
          >Read More
          <svg
            class="w-4 h-4 ml-2"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path d="M5 12h14"></path>
            <path d="M12 5l7 7-7 7"></path>
          </svg>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue, { PropOptions } from 'vue'

export default Vue.extend({
  props: {
    title: {
      type: String,
      required: true,
    } as PropOptions<string>,

    slug: {
      type: String,
      required: true,
    } as PropOptions<string>,

    description: {
      type: String,
      required: true,
    } as PropOptions<string>,

    createdAt: {
      type: String,
      required: true,
    } as PropOptions<string>,
  },
})
</script>

<style></style>
