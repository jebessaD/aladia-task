<template>
    <div class="border bg-white max-w-xl md:max-w-3xl mx-4 md:mx-20 mt-10 p-3 md:p-6">
        <h2 class="text-xl md:text-2xl font-bold mb-6">Frequently Bought Together</h2>

        <div v-for="(course, index) in courses" :key="index"
            class="flex items-center justify-between py-2 last:border-b-0">
            <div class="relative mr-4">
                <img :src="course.image" alt="Course image" class="w-24 h-24 object-cover md:h-auto md:w-52 rounded">
                <div v-if="index < courses.length - 1"
                    class="absolute right-1/2 -mr-4 mt-1 shadow-sm transform -translate-y-1/2 z-10 bg-white rounded-full p-1 border border-gray-300">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="size-8">
                        <path
                            d="M8.75 3.75a.75.75 0 0 0-1.5 0v3.5h-3.5a.75.75 0 0 0 0 1.5h3.5v3.5a.75.75 0 0 0 1.5 0v-3.5h3.5a.75.75 0 0 0 0-1.5h-3.5v-3.5Z" />
                    </svg>
                </div>

            </div>

            <div class="flex-1">
                <div class="flex w-full">
                    <h3 class="pr-2 md:pr-12 font-bold text-gray-900">{{ course.title }}</h3>
                    <div class="font-bold text-gray-900">{{ course.price }}</div>
                </div>

                <p class="text-gray-600 text-xs">{{ course.author }}</p>

                <div class="flex items-center text-gray-600 text-xs mt-1 space-x-1">
                    <div v-for="n in 5" :key="n">

                        <svg xmlns="http://www.w3.org/2000/svg" class="w-3 h-3 text-yellow-600" fill="currentColor"
                            viewBox="0 0 20 20">
                            <path
                                d="M10 15l-5.878 3.09 1.123-6.555L.49 6.82l6.586-.957L10 0l2.924 5.864 6.586.957-4.755 4.715 1.123 6.555z" />
                        </svg>

                    </div>

                    <span>({{ course.reviews.toLocaleString() }})</span>

                </div>

                <span>({{ course.reviews.toLocaleString() }})</span>
            </div>


        </div>

        <!-- Total Price and Button -->
        <div class="flex items-center justify-between pt-4 ">
            <span class="text-xl font-semibold">Total: <span class="text-gray-900">{{ totalPrice }}</span></span>
            <button class="px-4 py-3 bg-purple-600 text-white font-semibold hover:bg-purple-700 transition">Add
                all to cart</button>
        </div>
    </div>
</template>

<script>
import previewImage from "@/assets/images/preview.jpg";
import previewImage2 from "@/assets/images/preview4.jpg";
import previewImage3 from "@/assets/images/preview3.jpg";

export default {
    data() {
        return {
            courses: [
                {
                    image: previewImage,
                    title: "Google Cloud Professional Architect: Get Certified 2022",
                    author: "Dan Sullivan",
                    rating: 4.7,
                    reviews: 1632,
                    price: "$69.99",
                },
                {
                    image: previewImage3,
                    title: "Google Cloud Associate Cloud Engineer: Get Certified 2024",
                    author: "Dan Sullivan",
                    rating: 4.4,
                    reviews: 10881,
                    price: "$79.99",
                },
                {
                    image: previewImage2,
                    title: "Google Cloud Professional Data Engineer: Get Certified 2022",
                    author: "Dan Sullivan",
                    rating: 4.6,
                    reviews: 4214,
                    price: "$74.99",
                },
            ],
        };
    },
    computed: {
        totalPrice() {
            return "$" + this.courses.reduce((sum, course) => sum + parseFloat(course.price.slice(1)), 0).toFixed(2);
        },
    },
};
</script>


<style scoped>
/* Optional custom styles */
</style>