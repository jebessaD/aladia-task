<template>
    <div class="bg-white max-w-md md:max-w-3xl mx-20 mt-10 p-4">
      <!-- Requirements Section -->
      <div class="mb-6">
        <h2 class="text-2xl font-bold mb-4">Requirements</h2>
        <ul class="list-disc list-inside space-y-2 text-gray-800 text-sm">
          <li>Understand the basics of cloud computing</li>
          <li>Have some familiarity with networking</li>
          <li>Have some familiarity with software engineering</li>
        </ul>
      </div>
  
      <!-- Description Section -->
      <div>
        <h2 class="text-2xl font-bold mb-4">Description</h2>
        <div class="text-gray-800 text-sm leading-relaxed mb-4" v-html="displayDescription"></div>
        <div v-if="!showMore" class="h-16 -mt-16 blur-xl bg-white w-full relative overflow-hidden"></div>
        <!-- "Show more" button -->
        <button @click="showMore = !showMore" class="text-indigo-800 text-sm font-semibold hover:underline mt-4">
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
          <p>Get started in one of the most challenging and rewarding careers, cloud architecture. Cloud architects are in high demand and they are some of the top-paid certified professionals.</p>
          
          <p>Architects must have broad technical knowledge spanning compute, storage, networking, data analysis, software engineering, security, and DevOps. And that's not all -- architects must know how to work with sponsors, end users, and subject matter experts to define requirements and create a technical framework for developers, network engineers, data modelers, and other technical experts.</p>
  
          <p>This course is <strong>designed and developed by the author of the official Google Cloud Professional Architect exam guide</strong> and an architect with decades of experience in systems design, software engineering, data architecture, and machine learning. This course <strong>combines lectures with quizzes</strong> to ensure you understand the full breadth of the Google Cloud Professional Architect exam, including:</p>
  
          <ul class="list-disc list-inside ml-6 space-y-2">
            <li>Compute services including Compute Engine, App Engine, Kubernetes Engine, and Cloud Functions</li>
            <li>Storage services like Cloud Storage, Cloud SQL, Cloud Spanner, Firestore, Bigtable, BigQuery</li>
            <li>Data pipeline and analytic services, such as Cloud Dataflow, Cloud Data Fusion, Cloud Dataproc, and Vertex AI</li>
            <li>Networking services from Cloud Router and Cloud NAT to Private Service Connect and Data Loss Prevention Service</li>
            <li>Migrating to the cloud and migration strategies</li>
            <li>Security, from access controls and policies to regulations and compliance</li>
          </ul>
  
          <p>This course is designed to not only help you pass the Google Cloud Professional Architect exam but also to succeed as an architect. Learn how to think through architecture challenges, assess various options, balance business and technical requirements, and deliver highly scalable, reliable, and efficient systems.</p>
  
          <p>The course includes a 50-question practice exam that will test your knowledge of data engineering concepts and help you identify areas you may need to study more.</p>
  
          <p>By the end of this course, you will be ready to use Google Cloud services to design, deploy, and monitor applications, deploy advanced data management systems, design networks to support hybrid computing, ensure streamlined operations in the cloud, migrate workloads to the cloud, and much more.</p>
  
          <p class="font-bold uppercase text-lg mt-4">Are you ready to think like an architect and pass the Google Cloud Professional Architect Exam? Let's get started.</p>
  
          <h3 class="text-xl font-semibold mt-6">Who this course is for:</h3>
          <ul class="list-disc list-inside ml-6 space-y-2">
            <li>You are interested in getting started in cloud</li>
            <li>You want to become a Google Cloud Professional Architect</li>
            <li>You are an architect interested in learning about cloud</li>
            <li>Software engineers, DevOps engineers</li>
            <li>You want to become Google Cloud Certified Digital Leader</li>
          </ul>
        `,
        trimLength: 900, // Character length of the truncated text
      };
    },
    computed: {
      displayDescription() {
        // Show trimmed description if showMore is false, otherwise show full description
        return this.showMore
          ? this.fullDescription
          : this.fullDescription.slice(0, this.trimLength) + '...';
      },
    },
  };
  </script>
  
  <style scoped>
  /* Custom styles, if needed */
  </style>
  