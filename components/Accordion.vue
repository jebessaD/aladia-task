<template>
    <div class="accordion max-w-md md:max-w-3xl mx-20 mt-10">
        <h3 class="text-2xl text-gray-800 font-bold mb-6">Course content</h3>
        <div class="flex items-center justify-between py-3">
            <p class="text-sm text-gray-700">34 sections • 143 lectures • 8h 47m total length</p>
            <button class="text-violet-800 font-bold text-sm" @click="toggleAll">
                {{ allExpanded ? 'Collapse All sections' : 'Expand All sections' }}
            </button>
        </div>
        <div class="accordion-item border border-b-0 border-gray-300" v-for="(item, index) in accordionItems"
            :key="index">
            <div class="accordion-header" @click="toggleAccordion(index)">
                <svg class="w-4 h-4 transform transition-transform duration-300"
                    :class="{ 'rotate-180': isOpen[index] }" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
                <h3 class="text font-bold mr-auto ml-3">{{ item.title }}</h3>
                <p class="text-gray-700 text-sm">{{ item.time }}</p>
            </div>

            <div class="accordion-content" v-show="isOpen[index]">
                <p class="text-gray-700 text-sm">{{ item.content }}</p>
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
                { title: 'Course Orientation', time: '10 lectures • 31min', content: 'Introduction to the course and expectations.' },
                { title: 'An Introduction to Web Development', time: '8 lectures • 40min', content: 'Overview of web development and key concepts.' },
                { title: 'HTML: The Essentials', time: '13 lectures • 1hr 3min', content: 'Core HTML elements and structure.' },
                { title: 'HTML: Next Steps & Semantics', time: '9 lectures • 1hr 1min', content: 'Understanding semantic HTML for better structure.' },
                { title: 'HTML: Forms & Tables', time: '17 lectures • 1hr 45min', content: 'Creating forms and tables to collect and organize data.' },
                { title: 'CSS: The Very Basics', time: '11 lectures • 1hr', content: 'Introduction to CSS styling and syntax.' },
                { title: 'The World of CSS Selectors', time: '14 lectures • 1hr 10min', content: 'Using different CSS selectors for precision.' },
                { title: 'The CSS Box Model', time: '9 lectures • 1hr 8min', content: 'Understanding the box model and layout.' },
                { title: 'Other Assorted Useful CSS Properties', time: '11 lectures • 1hr 29min', content: 'Exploring additional CSS properties for styling.' },
                { title: 'CSS Flexbox: Designing Responsive Layouts', time: '12 lectures • 1hr 20min', content: 'Using Flexbox for flexible, responsive layouts.' },
                { title: 'CSS Grid: A Modern Layout Solution', time: '10 lectures • 1hr 45min', content: 'Mastering CSS Grid for complex layouts.' },
                { title: 'Responsive Web Design Basics', time: '8 lectures • 55min', content: 'Principles of responsive design for all devices.' },
                { title: 'Introduction to JavaScript', time: '15 lectures • 1hr 35min', content: 'JavaScript basics for interactivity on the web.' },
                { title: 'JavaScript: Control Flow and Functions', time: '14 lectures • 1hr 50min', content: 'Control structures and functions in JavaScript.' },
                { title: 'JavaScript DOM Manipulation', time: '13 lectures • 1hr 40min', content: 'Manipulating HTML with JavaScript DOM methods.' },
                { title: 'JavaScript: Events and User Interaction', time: '10 lectures • 1hr 5min', content: 'Handling user events for interactive pages.' },
                { title: 'Version Control with Git & GitHub', time: '6 lectures • 45min', content: 'Basics of Git and GitHub for project management.' },
                { title: 'Introduction to Web Accessibility', time: '9 lectures • 1hr', content: 'Making websites accessible for all users.' },
                { title: 'Introduction to Web Performance Optimization', time: '5 lectures • 35min', content: 'Improving website speed and performance.' },
                { title: 'Deploying Your Website', time: '7 lectures • 40min', content: 'Steps to launch your website online.' },
                { title: 'Course Wrap-Up & Final Thoughts', time: '4 lectures • 15min', content: 'Summing up the course and key takeaways.' }
            ],
        };
    },
    computed: {
        allExpanded() {
            return this.isOpen.every(status => status);
        },
    },
    methods: {
        toggleAccordion(index) {
            this.isOpen[index] = !this.isOpen[index];
        },
        toggleAll() {
            const expand = !this.allExpanded;
            this.isOpen = this.isOpen.map(() => expand);
        },
    },
};
</script>

<style scoped>
.accordion-header {
    @apply flex justify-between items-center cursor-pointer bg-gray-50 p-4 px-6;
}

.accordion-header h3 {
    @apply text-gray-800;
}

.accordion-header svg {
    @apply transition-transform duration-300 text-gray-700;
}

.accordion-content {
    @apply bg-white p-4;
    transition: max-height 0.3s ease-out;
    overflow: hidden;
}
</style>
