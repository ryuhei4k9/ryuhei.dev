<template>
  <div>
    <section class="text-gray-600 body-font overflow-hidden">
      <div class="px-5 py-12">
        <div class="-my-8 divide-y-2 divide-gray-100">
          <div class="py-8 flex flex-wrap md:flex-nowrap">
            <div class="md:flex-grow">
              <h1 class="text-3xl font-medium text-gray-900 title-font">
                ああああああああああああ
              </h1>
              <div class="leading-loose pt-6">
                <ul>
                  <li>twitter</li>
                </ul>
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
import Blog from '~/components/Blog.vue'

export default Vue.extend({
  components: {
    Header,
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
