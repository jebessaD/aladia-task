<template>
    <div class="bg-white max-w-xl md:max-w-3xl md:mx-20 mx-4 mt-4 p-4">
        <!-- Requirements Section -->
        <div class="">
            <h2 class="text-2xl font-bold mb-4">Instructor</h2>
            <h3 class="text-lg mb-1 font-bold text-purple-800 underline cursor-pointer">
                Dan Sullivan
            </h3>
            <p class="text-gray-600 mb-2">Cloud Architect, Data Engineer and Author</p>
        </div>
        <!-- Description Section -->
        <div class="flex items-center space-x-4 mb-4">
            <!-- Instructor Image -->
            <img src="@/assets/images/inst.jpg" alt="Instructor" class="w-28 h-28 rounded-full object-cover" />
            <!-- Instructor Details -->
            <div>

                <div class="flex flex-col space-y-1 my-2 mb-4 text-sm text-gray-700">
                    <div class="flex items-center space-x-2">
                        <span>⭐ 4.4 Instructor Rating</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <span>🎖️ 27,725 Reviews</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <span>👥 187,089 Students</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <span>🎓 12 Courses</span>
                    </div>
                </div>
            </div>
        </div>
        <div>

            <div class="text-gray-800 text-sm leading-relaxed mb-4" v-html="displayDescription"></div>
            <div v-if="!showMore" class="h-16 -mt-16 blur-xl bg-white w-full relative overflow-hidden"></div>
            <!-- "Show more" button -->
            <button @click="showMore = !showMore" class="text-indigo-800 text-sm font-bold hover:underline mt-4">
                {{ showMore ? 'Show less' : 'Show more' }}
            </button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showMore: false, // Toggle for "Show more" content
            fullDescription: `

            <p><i>Dan Sullivan is a cloud architect, systems developer, and author of the Official Google Cloud Professional Architect Study Guide, the Official Google Cloud Professional Data Engineer Study Guide, and the Official Google Cloud Associate Engineer Study Guide.</i></p>
            <br>
           
            <p> He is an experienced trainer and his online training courses have been viewed over 1 million times. Dan has extensive experience in multiple fields, including cloud architecture,  data architecture and modeling, machine learning, data science, and streaming analytics.</p>
        `,
            trimLength: 600, // Character length of the truncated text
        };
    },
    computed: {
        displayDescription() {
            // Show trimmed description if showMore is false, otherwise show full description
            return this.showMore
                ? this.fullDescription
                : this.fullDescription.slice(0, this.trimLength);
        },
    },
};
</script>

<style scoped>
/* Custom styles, if needed */
</style>