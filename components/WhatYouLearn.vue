<template>
  <div class="max-w-xl md:max-w-3xl px-4 border mx-4 md:mx-20 mt-10">
    <div class="p-6 text-xs">
      <h2 class="text-2xl font-bold mb-4">What you'll learn</h2>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 transition-all duration-300" :class="{
        'max-h-[220px] overflow-hidden': !isExpanded,
        'max-h-full': isExpanded
      }">
        <div v-for="(item, index) in learningItems" :key="index" class="flex items-start">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor"
            class="w-5 h-5 text-black mr-2 flex-shrink-0 mt-1">
            <path fill-rule="evenodd"
              d="M12.416 3.376a.75.75 0 0 1 .208 1.04l-5 7.5a.75.75 0 0 1-1.154.114l-3-3a.75.75 0 0 1 1.06-1.06l2.353 2.353 4.493-6.74a.75.75 0 0 1 1.04-.207Z"
              clip-rule="evenodd" />
          </svg>
          <p>{{ item }}</p>
        </div>
      </div>

      <div v-if="!isExpanded" class="h-16 -mt-12 blur-xl bg-white w-full relative overflow-hidden">

      </div>

      <div class="text-start">
        <button @click="toggleVisibility" class="text-purple-950 text-base bg-white font-bold hover:underline">
          {{ isExpanded ? 'Show Less' : 'Show More' }}
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      learningItems: ['The ins and outs of HTML5, CSS3, and Modern JavaScript for 2021', 'Make REAL web applications using cutting-edge technologies', 'Create responsive, accessible, and beautiful layouts', 'Recognize and prevent common security exploits like SQL-Injection & XSS', 'Continue to learn and grow as a developer, long after the course ends', 'Create a blog application from scratch using Node, Express, and MongoDB.', 'Create a complicated yelp-like application from scratch', 'Deploy your applications and work with cloud databases', 'Create static HTML and CSS portfolio sites and landing pages', 'Think like a developer. Become an expert at Googling code questions!', 'Create complex HTML forms with validations', 'Implement full authentication from scratch!', 'Use CSS Frameworks including Bootstrap 5, Semantic UI, and Bulma', 'Implement responsive navbars on websites', 'Use JavaScript variables, conditionals, loops, functions, arrays, and objects', 'Write Javascript functions, and understand scope and higher order functions', 'Master the "weird" parts of JavaScript', 'Create full-stack web applications from scratch', 'Manipulate the DOM with vanilla JS', 'Write JavaScript based browser games'],
      isExpanded: false,
    };
  },
  methods: {
    toggleVisibility() {
      console.log('Toggling visibility');
      this.isExpanded = !this.isExpanded;
    }
  }
};
</script>
