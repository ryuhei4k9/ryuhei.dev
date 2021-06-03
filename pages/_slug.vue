<template>
  <div>
    <section class="text-gray-600 body-font overflow-hidden">
      <div class="px-5 py-12">
        <div class="-my-8 divide-y-2 divide-gray-100">
          <div class="py-8 flex flex-wrap md:flex-nowrap">
            <div class="md:flex-grow">
              <h1 class="text-3xl font-medium text-gray-900 title-font">
                {{ article.title }}
              </h1>
              <span class="text-gray-500 text-sm">{{
                dateFormat(article.createdAt)
              }}</span>
              <div class="leading-loose pt-6">
                <nuxt-content :document="article" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Context } from '@nuxt/types'

import Header from '~/components/Header.vue'

export default Vue.extend({
  components: {
    Header,
  },

  async asyncData({ $content, params }: Context) {
    const article = await $content(params.slug).fetch()
    return { article }
  },

  methods: {
    dateFormat(dateString: string) {
      return this.$dayjs(dateString).format('YYYY/MM/DD')
    },
  },
})
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/

.nuxt-content h2 {
  @apply text-2xl font-medium mt-8 mb-4;
}

.nuxt-content p {
  @apply leading-8 mb-4;
}
</style>
