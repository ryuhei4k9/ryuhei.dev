<template>
  <div>
    <Blog :articles="articles" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Context } from '@nuxt/types'
import Blog from '~/components/Blog.vue'

export default Vue.extend({
  components: {
    Blog,
  },

  async asyncData({ $content }: Context) {
    const articles = await $content()
      .only(['title', 'slug', 'description', 'createdAt'])
      .sortBy('createdAt', 'desc')
      .fetch()
    return {
      articles,
    }
  },
})
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
