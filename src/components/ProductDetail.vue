User
<template>
        <!-- <div class="lg:mt-8 lg:flex items-center lg:w-[1103px] lg:h-[400px] lg:p-[48px 64px] lg:rounded-[40px] lg:border-[0px 0px 6px 0px] lg:gap-64 bg-[#FFE58C] -->
        <!-- sm:w-[Hug_(347px)] sm:h-[Hug_(766px)] sm:gap-10 s:pl-8 sm:pr-[32px] sm:pt-[32px] sm:pb-[40px] sm:rounded-2xl sm:border-[0px] sm:border-[6px,0px] -->
<!-- "> -->
<div class="flex flex-wrap bg-[#FFE58C] lg:mt-8">
     <!-- <div class=" w-[465px] h-[318px] gap-48 p-4"> -->
      <div class="p-4 mr-10 ml-8">
      <div class="mt-4 w-[465px] h-[58px] text-5xl font-semibold leading-[58px] tracking-normal text-left">{{ productData.title }}</div>
      <div class=" mt-4 w-[465px] h-[124px]  text-2xl font-normal leading-[31px] tracking-normal text-left sm:w-[283px] sm:h-28">{{ productData.content }}</div>
      <div>
        <button class="lg:mt-10 lg:w-[262px] lg:h-[64px] left-[-16.5px] gap-2 pl-11 pr-[44px] py-[20px] text-xl font-semibold leading-6 tracking-normal text-left rounded-[40px] border-[3px] border-black bg-[#F15A29] sm:w-[229px] sm:h-[64px]
">
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