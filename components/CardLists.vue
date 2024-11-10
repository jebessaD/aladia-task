<template>
    <div class=" max-w-xl md:max-w-3xl mx-4 md:mx-20 mt-10">
        <h2 class="text-2xl font-bold mb-2">More Courses by <span class="text-violet-800">Dan Sullivan</span> </h2>
        <div class="grid border-b pb-4 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-2">
            <div v-for="(course, index) in courses" :key="index"
                class="flex flex-col items-start p-4 text-xs">
                <img :src="course.image" alt="Course Image" class="w-full h-32 object-cover rounded-md mb-4" />
                <h3 class="text-base font-semibold">{{ course.title }}</h3>
                <p class="text-gray-600 text-xs">by {{ course.author }}</p>

                <div class="flex items-start mt-2 text-base">
                    <p class="font-semibold mr-1">{{ course.rating }}</p>
                    <span class="text-yellow-600" v-for="n in Math.floor(course.rating)" :key="n">★</span>
                    <span class="text-gray-400" v-for="n in 5 - Math.floor(course.rating)" :key="n">★</span>
                    <span class="text-gray-500 ml-2 text-sm">({{ course.ratingCount }})</span>
                </div>

                <p class="text-gray-500 mt-1">
                    {{ course.hours }} total hours - {{ course.lectures }} lectures - All Levels
                </p>

                <p class="text-base font-bold mt-2">${{ course.price }}</p>
            </div>
            
        </div>
        <button class="w-full mt-4 border border-black py-2 mb-10 text-sm">Report Abuse</button>
       
    </div>
</template>

<script>
import previewImage from "@/assets/images/preview3.jpg";
import previewImage2 from "@/assets/images/preview2.jpg";
import previewImage3 from "@/assets/images/preview4.jpg";

export default {
    
    data() {
        return {
            courses: [
                {
                    image: previewImage,
                    title: "Google Cloud Associate Cloud Engineer: Get...",
                    author: "Dan Sullivan",
                    rating: 4.4,
                    ratingCount: 10883,
                    hours: 8.5,
                    lectures: 114,
                    price: 79.99,
                },
                {
                    image: previewImage2,
                    title: "Google Cloud Machine Learning Engineer...",
                    author: "Dan Sullivan",
                    rating: 4.3,
                    ratingCount: 978,
                    hours: 5.5,
                    lectures: 71,
                    price: 64.99,
                },
                {
                    image:previewImage3,
                    title: "Google Cloud Professional Data Engineer: Get Certified...",
                    author: "Dan Sullivan",
                    rating: 4.6,
                    ratingCount: 4216,
                    hours: 6.5,
                    lectures: 115,
                    price: 74.99,
                },
            ],
        };
    },
};
</script>

<style scoped></style>