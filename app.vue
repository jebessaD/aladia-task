<template>
  <div class=" relative">
    <Header />
    <div ref="courseCard" class="absolute top-28 right-20 " :class="{ 'fixed': isSticky }"
      :style="stickyStyle">
      <CourseCard />
    </div>
    <NuxtPage>

      <WebDeveloperBootcamp title="Google Cloud Professional Architect: Get Certified 2022" :rating="4.7"
        :numRatings="276801" :numStudents="924037" instructor="Dan Sullivan" />

      <div class="px-5">
        <CertificationCard />
        <WhatYoullLearn />
        <CourseInfoCard />
        <CompanyOfferSection />
        <AccordionVue />
        <CourseDescription />
        <StudentAlsoBought />
        <FrequentlyBoughtTogether />
        <InstructorCard />
        <Reviews />
        <CardList />

      </div>
      <ExloreSkills />

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
import CertificationCard from './components/CertificationCard.vue';
import CourseInfoCard from '~/components/CourseInfoCard.vue'
import CompanyOfferSection from '~/components/CompanyOfferSection.vue'
import CourseDescription from '~/components/CourseDescription.vue'
import StudentAlsoBought from '~/components/StudentsAlsoBought.vue'
import FrequentlyBoughtTogether from '~/components/FrequentlyBoughtTogether.vue'
import InstructorCard from '~/components/InstructorCard.vue'
import Reviews from '~/components/Reviews.vue'
import CardList from '~/components/CardLists.vue'
import ExloreSkills from '~/components/ExploreSkills.vue'

export default {
  components: {
    Header,
    Footer,
    WebDeveloperBootcamp,
    CourseCard,
    WhatYoullLearn,
    AccordionVue,
    CertificationCard,
    CourseInfoCard,
    CompanyOfferSection,
    StudentAlsoBought,
    FrequentlyBoughtTogether,
    Reviews,
    CardList,
    ExloreSkills
  },

};
</script>
