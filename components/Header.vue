<template>
  <header class="text-gray-600 body-font">
    <div
      class="
        container
        mx-auto
        flex flex-wrap
        p-5
        flex-col
        md:flex-row
        items-center
      "
    >
      <nuxt-link
        to="/"
        class="
          flex
          title-font
          font-medium
          items-center
          text-yellow-500
          hover:text-yellow-600
          mb-4
          md:mb-0
        "
      >
        <!-- <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          class="w-10 h-10 text-white p-2 bg-yellow-500 rounded-full"
          viewBox="0 0 24 24"
        >
          <path
            d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"
          ></path>
        </svg> -->
        <img
          src="https://github.com/ryuhei4k9.png"
          width="32"
          height="32"
          alt="potato4d"
          class="rounded-full inline-block mr-3"
        />
        <span class="text-xl">ryuhei.dev</span>
      </nuxt-link>
      <nav
        class="md:ml-auto flex flex-wrap items-center text-base justify-center"
      >
        <nuxt-link to="about" class="mr-5 hover:text-gray-900">About</nuxt-link>
        <nuxt-link to="portfolio" class="hover:text-gray-900"
          >Portfolio</nuxt-link
        >
      </nav>
    </div>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style></style>
