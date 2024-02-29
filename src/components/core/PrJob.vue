<template>
  <pr-card>
    <header class="job_header">
      <img class="job_picture" :src="job.enterprise.picture" :alt="job.enterprise.name">
      <section class="job_info">
        <strong>{{ job.enterprise.name }}</strong>
        <p>{{ job.enterprise.position }}</p>
        <p>{{ get_date() }}</p>
      </section>
    </header>
    <main class="job_description">
      <section>
        <h3>Funciones a cargo</h3>
        <p>
          <ol>
            <li v-for="job_function in job.functions">- {{ job_function }}</li>
          </ol>
        </p>
      </section>
      <section>
        <h3>
          Productos digitales
        </h3>
        <p>
          <ol>
            <li v-for="job_product in job.products">- {{ job_product }}</li>
          </ol>
        </p>
      </section>
    </main>
  </pr-card>
</template>

<script setup>
  import PrCard from './PrCard.vue';

  const props = defineProps(['job'])

  const get_date = () => {
    const dates = props.job.enterprise.date
    return `${dates.start} - ${dates.end}`
  }
</script>

<style scoped>
  .job_header {
    display: flex;
  }
  .job_picture {
    width: 85px;
    margin-right: 10px;
  }
  .job_info {
    color: #7D7D7D;
  }
  .job_info strong {
    color: black;
  }
  .job_description {
    margin: 20px 0px;
  }
  .job_description p {
    margin: 10px 0px;
  }
  .job_description ol {
    padding: 0px;
  }
  .job_description li {
    list-style: none;
    color: #7D7D7D;
  }
</style>