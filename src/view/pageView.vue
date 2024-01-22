<template>
  <div class="m-4">
  <h1 class="head_text my-8">
  Section Title
  <br />
  <div class="head_subtitle text-center">Section Subtitle</div>
  </h1>
  <ProductView />
  </div>
  </template>
  
  <script>
  import ProductView from "./productView.vue";
  
  export default {
  name: "pageView",
  components: { ProductView },
  };
  </script>