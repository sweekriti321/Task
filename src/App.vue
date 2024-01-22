<template>
  <div class="flex justify-center">
  <pageView />
  </div>
  </template>
  
  <script>
  import pageView from "@/view/pageView.vue";
  
  export default {
  name: "App",
  components: {
  pageView,
  },
  };
  </script>