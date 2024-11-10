<template>
    <div class="border bg-white max-w-xl md:max-w-3xl mx-4 md:mx-20 mt-10 p-4">
      <!-- Heading and Description -->
      <div class="mb-4">
        <h3 class="text-lg font-semibold text-gray-800">Top companies offer this course to their employees</h3>
        <p class="text-gray-600 text-sm">
          This course was selected for our collection of top-rated courses trusted by businesses worldwide.
          <a href="#" class="text-violet-800 hover:underline">Learn more</a>
        </p>
      </div>
  
      <!-- Company Logos -->
      <div class="flex items-center flex-wrap justify-around mt-6 space-x-4">
        <img src="@/assets/images/nasdaq-logo.png" alt="Nasdaq" class="h-10">
        <img src="@/assets/images/volkswagen-logo.png" alt="Volkswagen" class="h-10">
        <img src="@/assets/images/box.jpg" alt="Box" class="h-10">
        <img src="@/assets/images/netapp.jpg" alt="NetApp" class="h-10">
        <img src="@/assets/images/eventbit.jpg" alt="Eventbrite" class="h-10">
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CompanyOfferSection',
  }
  </script>
  