<template>
    <div class="border bg-white max-w-md md:max-w-3xl mx-20 mt-10">
        <div class="mb-2 text-gray-800 font-bold bg-gray-100 p-4">
            Prepare for your certification with this course.
            <a href="#" class="text-violet-800 underline hover:underline">Learn more</a>
        </div>
        <div class="flex items-center space-x-4 p-4">
            <nuxt-link to="/" class="text-gray-800 font-bold text-lg w-16 flex ">
                <img class="w-full" src="@/assets/images/google.png" alt="google clould">
            </nuxt-link>
            <!-- <img src="https://path/to/google-cloud-icon.png" alt="Google Cloud Logo" class="w-12 h-12" /> -->
            <div>
                <h2 class="font-bold text-violet-800">
                    Professional Cloud Architect
                </h2>
                <p class="text-gray-500 text-sm">Issued by Google Cloud</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CertificationCard',
}
</script>