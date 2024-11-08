<template>
    <div class="accordion max-w-md md:max-w-3xl mx-20 mt-10">
        <div class="accordion-item border-b border-gray-300" v-for="(item, index) in accordionItems" :key="index">
            <div class="accordion-header" @click="toggleAccordion(index)">
                <h3 class="text-lg font-bold">{{ item.title }}</h3>
                <svg class="w-6 h-6 transform transition-transform duration-300" :class="{ 'rotate-180': isOpen[index] }" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
            </div>
          
            <div class="accordion-content" v-show="isOpen[index]">
                <p class="text-gray-400">{{ item.content }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            
            isOpen: Array(9).fill(false), 
            accordionItems: [
                { title: 'Course Orientation', content: '10 lectures • 31min' },
                { title: 'An Introduction to Web Development', content: '8 lectures • 40min' },
                { title: 'HTML: The Essentials', content: '13 lectures • 1hr 3min' },
                { title: 'HTML: Next Steps & Semantics', content: '9 lectures • 1hr 1min' },
                { title: 'HTML: Forms & Tables', content: '17 lectures • 1hr 45min' },
                { title: 'CSS: The Very Basics', content: '11 lectures • 1hr' },
                { title: 'The World of CSS Selectors', content: '14 lectures • 1hr 10min' },
                { title: 'The CSS Box Model', content: '9 lectures • 1hr 8min' },
                { title: 'Other Assorted Useful CSS Properties', content: '11 lectures • 1hr 29min' },
            ],
        };
    },
    methods: {
        toggleAccordion(index) {
            console.log('Toggling index:', index);
            this.isOpen[index] = !this.isOpen[index]; 
        },
    },
};
</script>


<style scoped>
.accordion-header {
    @apply flex justify-between items-center cursor-pointer bg-gray-100 p-4;
}

.accordion-header h3 {
    @apply text-gray-800;
}

.accordion-header svg {
    @apply transition-transform duration-300 text-gray-500;
}

.accordion-content {
    @apply bg-white p-4;
    transition: max-height 0.3s ease-out;
    overflow: hidden;
}
</style>
