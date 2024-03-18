<template>
    <pr-page-template title="Portfolio" logo="portfolio">
      <section class="pt-grid">
        <pr-flip-card v-for="prod in prods" :prod="prod"/>
      </section>
    </pr-page-template>
  </template>
  
  <script setup>
  
  import PrPageTemplate from '@/components/core/PrPageTemplate.vue';
  import PrFlipCard from '@/components/core/PrFlipCard.vue';
  
  const prods = [
    {
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"Uber",
      picture:"https://pbs.twimg.com/profile_images/1042867341476995078/antCC8gJ_400x400.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam rem natus debitis placeat, vitae possimus? Architecto rerum ipsum, ad quasi nemo atque ab quo nam necessitatibus, quod minus repellat porro. Lorem impsu dolor sit amep",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    },{
      title:"discovery app",
      picture:"https://is4-ssl.mzstatic.com/image/thumb/Purple118/v4/82/58/59/8258596e-9969-c19e-d0b1-ee26abd8bd4a/source/512x512bb.jpg",
      tags: ["niños", "entretenimiento", "applicación"],
      description: "lorem impsum",
      link: "/portafolio/1"
    }
  ]
  </script>
  
  <style scoped>
    h3 {
      font-size: 32px;
    }
    .pt-grid {
      display: grid;
      grid-template-columns: auto auto auto;
      grid-gap: 40px; 
    }
  </style>