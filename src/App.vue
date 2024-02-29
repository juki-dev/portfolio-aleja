<script setup>
import { RouterView } from 'vue-router'
import PrCard from './components/core/PrCard.vue'
import PrMenu from './components/PrMenu.vue'
import PrSkill from './components/PrSkill.vue'
import PrPresentation from './components/PrPresentation.vue'
</script>

<template>
  <header>

      <pr-card>
        <pr-presentation />
      </pr-card>

      <pr-card>
        <pr-menu />
      </pr-card>
      <pr-skill />
      
  </header>
  <main>
    <RouterView />
  </main>
</template>

<style scoped>

header {
  line-height: 1.5;
  max-height: 100vh;
  width: 350px;
}

main {
  flex: 5;
}

</style>