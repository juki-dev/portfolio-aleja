<template>
    <pr-page-template title="Work Experience" logo="experience">
      <pr-job v-for="job in job_list" :job="job"></pr-job>
    </pr-page-template>
  </template>
  
  <script setup>
  
  import PrJob from '@/components/core/PrJob.vue';
  import PrPageTemplate from '@/components/core/PrPageTemplate.vue';

  const job_list = [
    {
      enterprise: {
        name: "Tecno Makers SAS",
        picture: "https://www.tecno-makers.com/themes/onepage/front-logo.svg",
        position: "Ux Writter",
        date: {
          start: "May 2020",
          end: "Feb 2021"
        }
      },
      functions: [
        "Ux Writting interfaces for Discovery+ and Discovery Kids LATAM"
      ],
      products: [
        "Discovery+",
        "Discovery kids LATAM"
      ],
    },
    {
      enterprise: {
        name: "Start Up La Haus",
        picture: "https://www.tecno-makers.com/themes/onepage/front-logo.svg",
        position: "Creative Copywriter",
        date: {
          start: "May 2020",
          end: "Feb 2021"
        }
      },
      functions: [
        "Ux Writting for real state software development",
        "Copywriting for mails, sms and online advertising in Bogotá, Medellin and Mexico city"
      ],
      products: [
        "Real state project launcher",
        "Redesing and Write the new page"
      ],
    }
  ]
  </script>
  
  <style scoped>
    h3 {
      font-size: 32px;
    }
  </style>