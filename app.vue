<template>
  <div class=" relative">
    <Header />
    <div ref="courseCard" class="absolute bg-red-100 top-16 right-20 " :class="{ 'fixed': isSticky }"
      :style="stickyStyle">
      <CourseCard />
    </div>
    <NuxtPage>
      <WebDeveloperBootcamp title="The Web Developer Bootcamp 2024" :rating="4.7" :numRatings="276801"
        :numStudents="924037" instructor="Colt Steele" />
      <WhatYoullLearn />

      <AccordionVue />
    </NuxtPage>
    <Footer />
  </div>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue';
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import WebDeveloperBootcamp from '~/components/WebDeveloperBootcamp.vue';
import CourseCard from '~/components/CourseCard.vue';
import WhatYoullLearn from '~/components/WhatYouLearn.vue';
import AccordionVue from './components/Accordion.vue';

export default {
  components: {
    Header,
    Footer,
    WebDeveloperBootcamp,
    CourseCard,
    WhatYoullLearn,
    AccordionVue
  },

};
</script>
