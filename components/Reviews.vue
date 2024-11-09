<!-- Reviews.vue -->
<template>
    <div class="max-w-md md:max-w-3xl mx-20 mt-4 p-4">
      <h2 class="text-2xl font-bold">⭐ 4.7 course rating • 2K ratings</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <ReviewCard
          v-for="(review, index) in reviews"
          :key="index"
          :reviewerName="review.reviewerName"
          :rating="review.rating"
          :date="review.date"
          :comment="review.comment"
        />
      </div>
      <div class="flex justify-start mt-4">
            <button class="px-3 font-bold text-sm text-gray-800 py-2 border border-black  transition">
                Show all reviews
            </button>
        </div>
      
    </div>
  </template>
  
  <script>
  import ReviewCard from "./ReviewCard.vue";
  
  export default {
    name: "Reviews",
    components: {
      ReviewCard,
    },
    data() {
      return {
        reviews: [
          {
            reviewerName: "Laxman R.",
            rating: 5,
            date: "a week ago",
            comment: "Superb",
          },
          {
            reviewerName: "Vince N.",
            rating: 5,
            date: "a month ago",
            comment: "Thoroughly enjoyed this course and how well articulated the content was.",
          },
          {
            reviewerName: "Sandeep Kumar P.",
            rating: 4,
            date: "3 months ago",
            comment: "Found this course quite exciting",
          },
          {
            reviewerName: "Nirbhay S.",
            rating: 5,
            date: "5 months ago",
            comment:
              "This course provides an excellent foundation, but it is not sufficient on its own to pass the exam. The exam questions are quite difficult. To better prepare, consider taking this course along with some basic hands-on and practice.",
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Add custom styles if needed */
  </style>
  