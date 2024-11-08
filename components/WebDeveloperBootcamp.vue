<template>
  <div class="bg-neutral-900 text-white p-10 flex w-full">
    <div class="container flex flex-col space-y-3 px-20 mr-auto w-7/12 text-start justify-start">
      <div class="flex items-center justify-between">
        <div class="breadcrumb text-blue-200 font-semibold text-sm mb-10">
          <nuxt-link to="/development" class="hover:text-gray-300">Development</nuxt-link>
          <span class="mx-2">&gt;</span>
          <nuxt-link to="/web-development" class="hover:text-gray-300">Web Development</nuxt-link>
          <span class="mx-2">&gt;</span>
          <span>Web Development</span>
        </div>



      </div>

      <h1 class="text-3xl font-bold my-4">{{ title }}</h1>
      <h2 class="text-lg ">10 Hours of React just added. Become a Developer With ONE course - HTML, CSS, JavaScript,
        React, Node,
        MongoDB and More!</h2>
      <div class="rating flex items-center mt-10 text-xs">

        <div class="text-yellow-400"> 4.7 <span>⭐</span>
          <span>⭐</span>
          <span>⭐</span>
          <span>⭐</span>
        </div>

        <div class="flex items-center text-blue-200 text-sm"> <span class="">( {{ numRatings }} ratings )</span>
          <p class="text-white ml-1">{{ formattedNumStudents }} students</p>

        </div>
      </div>


      <div class=" mt-2 text-sm">Created by <nuxt-link to="/teach" class="text-blue-200 hover:text-gray-600">
          {{ instructor }}
        </nuxt-link> </div>

      <div class="flex justify-between items-center py-2">
        <div class="flex items-center ">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="size-5">
            <path fill-rule="evenodd"
              d="M18 10a8 8 0 1 1-16 0 8 8 0 0 1 16 0Zm-8-5a.75.75 0 0 1 .75.75v4.5a.75.75 0 0 1-1.5 0v-4.5A.75.75 0 0 1 10 5Zm0 10a1 1 0 1 0 0-2 1 1 0 0 0 0 2Z"
              clip-rule="evenodd" />
          </svg>


          <p class="text-xs mr-2">Last updated 10/2024</p>
          <div class="flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="size-4">
              <path fill-rule="evenodd"
                d="M3.757 4.5c.18.217.376.42.586.608.153-.61.354-1.175.596-1.678A5.53 5.53 0 0 0 3.757 4.5ZM8 1a6.994 6.994 0 0 0-7 7 7 7 0 1 0 7-7Zm0 1.5c-.476 0-1.091.386-1.633 1.427-.293.564-.531 1.267-.683 2.063A5.48 5.48 0 0 0 8 6.5a5.48 5.48 0 0 0 2.316-.51c-.152-.796-.39-1.499-.683-2.063C9.09 2.886 8.476 2.5 8 2.5Zm3.657 2.608a8.823 8.823 0 0 0-.596-1.678c.444.298.842.659 1.182 1.07-.18.217-.376.42-.586.608Zm-1.166 2.436A6.983 6.983 0 0 1 8 8a6.983 6.983 0 0 1-2.49-.456 10.703 10.703 0 0 0 .202 2.6c.72.231 1.49.356 2.288.356.798 0 1.568-.125 2.29-.356a10.705 10.705 0 0 0 .2-2.6Zm1.433 1.85a12.652 12.652 0 0 0 .018-2.609c.405-.276.78-.594 1.117-.947a5.48 5.48 0 0 1 .44 2.262 7.536 7.536 0 0 1-1.575 1.293Zm-2.172 2.435a9.046 9.046 0 0 1-3.504 0c.039.084.078.166.12.244C6.907 13.114 7.523 13.5 8 13.5s1.091-.386 1.633-1.427c.04-.078.08-.16.12-.244Zm1.31.74a8.5 8.5 0 0 0 .492-1.298c.457-.197.893-.43 1.307-.696a5.526 5.526 0 0 1-1.8 1.995Zm-6.123 0a8.507 8.507 0 0 1-.493-1.298 8.985 8.985 0 0 1-1.307-.696 5.526 5.526 0 0 0 1.8 1.995ZM2.5 8.1c.463.5.993.935 1.575 1.293a12.652 12.652 0 0 1-.018-2.608 7.037 7.037 0 0 1-1.117-.947 5.48 5.48 0 0 0-.44 2.262Z"
                clip-rule="evenodd" />
            </svg>

            <p class="text-xs">English</p>
          </div>
        </div>
        <div class="flex items-center mr-4">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="size-4">
            <path d="M2.5 3A1.5 1.5 0 0 0 1 4.5V5h14v-.5A1.5 1.5 0 0 0 13.5 3h-11Z" />
            <path fill-rule="evenodd"
              d="M15 7H1v4.5A1.5 1.5 0 0 0 2.5 13h11a1.5 1.5 0 0 0 1.5-1.5V7ZM3 10.25a.75.75 0 0 1 .75-.75h.5a.75.75 0 0 1 0 1.5h-.5a.75.75 0 0 1-.75-.75Zm3.75-.75a.75.75 0 0 0 0 1.5h2.5a.75.75 0 0 0 0-1.5h-2.5Z"
              clip-rule="evenodd" />
          </svg>

          <p class="text-xs">English [Auto]</p>
        </div>
        <div class="flex items-center">
          <language-icon class="h-4 w-4 mr-2" />
          <p class="text-xs">Arabic [Auto]</p>
        </div>
        <div class="ml-4 cursor-pointer">
          <chevron-down-icon class="h-4 w-4" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {  LanguageIcon, ChevronDownIcon } from '@heroicons/vue/24/solid'
export default {

  name: 'WebDeveloperBootcamp',
  components: {

    LanguageIcon,
    ChevronDownIcon
  },
  props: {
    title: {
      type: String,
      required: true
    },
    rating: {
      type: Number,
      required: true
    },
    numRatings: {
      type: Number,
      required: true
    },
    numStudents: {
      type: Number,
      required: true
    },
    instructor: {
      type: String,
      required: true
    }
  },
  computed: {
    // Format numRatings and numStudents with commas
    formattedNumRatings() {
      return this.numRatings.toLocaleString();
    },
    formattedNumStudents() {
      return this.numStudents.toLocaleString();
    }
  }
}
</script>

<style scoped>
/* Additional styling can go here */
</style>