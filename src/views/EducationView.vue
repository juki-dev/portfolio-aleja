<template>
  <pr-page-template title="Education" logo="education">
    <pr-card class="pr-education">
        <div v-for="education in formalEducation" class="pr-education_item">
          <h5>{{ education.institution }}</h5>
          <p v-for="program in education.programs">
            {{ program.years }} | {{ program.title }}
          </p>
        </div>
    </pr-card>
    <pr-card  class="pr-education">
        <h4 class="pr-education_title">Aditional Training</h4>
        <div v-for="education in aditionalEducation" class="pr-education_item">
          <h5>{{ education.institution }}</h5>
          <p v-for="program in education.programs">
            {{ program.years }} | {{ program.title }}
          </p>
        </div>
    </pr-card>
  </pr-page-template>
</template>

<script setup>

import PrPageTemplate from '@/components/core/PrPageTemplate.vue';
import PrCard from '@/components/core/PrCard.vue';

const formalEducation = [
  {institution: 'SENA | Servicio Nacional de Aprendize', programs: [{years: 'In progress', title: 'Information Systems and Development'}]},
  {institution: 'Universidad de Bogotá Jorge Tadeo Lozano', programs: [{years: '2011 - 2016', title: 'Journalism and Social Communication'}]},
]

const aditionalEducation = [
  {institution: 'UX en español', programs: [{years: '2021', title: 'Masterclass UX Content Testing'}]},
  {institution: 'Linked In', programs: [{years: '2020', title: 'Branding fundamentals'}]},
  {institution: 'Alcaldia Mayor de Bogotá', programs: [{years: '2019', title: 'Course in Artificail Intelligence (Basic Level)'}, {years: '2019', title: 'Course in Big Data (Basic Level)'}]},
  {institution: 'Partners Academy', programs: [{years: '2019', title: 'Digital Marketing & Digital Bussines Diplomat'}]},
  {institution: 'SENA', programs: [{years: '2016', title: 'Course in Digital Imaging'}]},
]

</script>

<style scoped>
  .pr-education_item h5{
    font-size: 16px;
    margin-bottom: 5px;
  }
  .pr-education .pr-education_title {
    font-size: 20px;
    font-weight: 1000;
    margin-bottom: 20px;
  }
  .pr-education_item {
    margin-bottom: 10px;
  }
  .pr-education_item p {
    color: #7D7D7D;
  }
</style>