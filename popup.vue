<template>
  <div>
    <header class="text-gray-600 body-font">
      <div
        class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
        <a
          class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="w-10 h-10 text-white p-2 bg-indigo-500 rounded-full"
            viewBox="0 0 24 24">
            <path
              d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path>
          </svg>
          <span class="ml-3 text-xl">Tailblocks</span>
        </a>
        <nav
          class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
          <a class="mr-5 hover:text-gray-900">First Link</a>
          <a class="mr-5 hover:text-gray-900">Second Link</a>
          <a class="mr-5 hover:text-gray-900">Third Link</a>
          <a class="mr-5 hover:text-gray-900">Fourth Link</a>
        </nav>
        <button
          class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0">
          Button
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="w-4 h-4 ml-1"
            viewBox="0 0 24 24">
            <path d="M5 12h14M12 5l7 7-7 7"></path>
          </svg>
        </button>
      </div>
    </header>
    <h2 class="text-center">
      Welcome to your
      <a href="https://www.plasmo.com" target="_blank">Plasmo</a> Extension!
    </h2>

    <div class="container">
      <button @click="decrement">-</button>
      <p>
        <b>{{ state.count }}</b>
      </p>
      <button @click="increment">+</button>
    </div>
  </div>
  <p v-if="state.action" class="action text-center">
    {{ state.action }}
  </p>
  <a href="https://docs.plasmo.com" target="_blank"> View Docs </a>
</template>

<script setup>
import { reactive } from "vue"

const state = reactive({ count: 0, action: null })

function increment() {
  state.count++
  state.action = "increment"
}

function decrement() {
  state.count--
  state.action = "decrement"
}
</script>

<style scoped>
@import './main.css';
</style>