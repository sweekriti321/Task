User
<template>
        <!-- <div class="lg:mt-8 lg:flex items-center lg:w-[1103px] lg:h-[400px] lg:p-[48px 64px] lg:rounded-[40px] lg:border-[0px 0px 6px 0px] lg:gap-64 bg-[#FFE58C] -->
        <!-- sm:w-[Hug_(347px)] sm:h-[Hug_(766px)] sm:gap-10 s:pl-8 sm:pr-[32px] sm:pt-[32px] sm:pb-[40px] sm:rounded-2xl sm:border-[0px] sm:border-[6px,0px] -->
<!-- "> -->
<div class="flex flex-wrap bg-[#FFE58C] lg:mt-8">
     <!-- <div class=" w-[465px] h-[318px] gap-48 p-4"> -->
      <div class="p-4 sm:mr-4 sm:ml-8 md:ml-12 lg:ml-16">
  <div class="productDetailTitle">{{ productData.title }}</div>
  <div class="productDetailContent">{{ productData.content }}</div>
  <div>
    <button class="productDetailBtn">
      Discover Product
    </button>
  </div>
</div>
     <!-- </div> -->
     <div>
      <Accordion />
     </div>
    </div>
    <!-- </div> -->
</template>

<script>
import Accordion from "@/components/Accordion.vue";
export default{
    name:"prodctDetail",
    props:{
        productData:{
            type: Object,
            required: true
        }
    },
    components: {
    Accordion
  }

}
</script>