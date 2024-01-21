<template>
  <!-- <div class="w-[900px] h-[1128.45px] top-[153px] left-[256px] rounded-[0px,0px,180px,0px] flex justify-center ">  -->
    <!-- <div class="lg:w-[486px] lg:h-[91.6px] lg:top-[153px] left-[621px] gap-[14px] bg-[#F7F7F7] md:shrink-0"> -->
      <div class="flex justify-center">
      <page-view />
    <!-- </div> -->
  </div>
</template>

<script>
import pageView from '@/view/pageView.vue';

export default {
  name: 'App',
  components: {
    pageView
  }
}
</script>
