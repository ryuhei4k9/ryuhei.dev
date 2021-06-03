<template>
  <section class="text-gray-600 body-font overflow-hidden">
    <div class="container px-5 py-12 mx-auto">
      <div class="-my-8 divide-y-2 divide-gray-100">
        <Article
          v-for="article in articles"
          :key="article.slug"
          :title="article.title"
          :slug="article.slug"
          :description="article.description"
          :created-at="dateFormat(article.createdAt)"
        />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue, { PropOptions } from 'vue'
import { IContentDocument } from '@nuxt/content/types/content'
import Article from './Article.vue'

export default Vue.extend({
  components: { Article },

  props: {
    articles: {
      type: Array,
      required: true,
    } as PropOptions<IContentDocument[]>,
  },

  methods: {
    dateFormat(dateString: string) {
      return this.$dayjs(dateString).format('YYYY/MM/DD')
    },
  },
})
</script>

<style></style>
