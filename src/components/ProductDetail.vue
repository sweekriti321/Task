
<template>
<div class="flex flex-wrap lg:rounded-[40px] lg:border-[0px 0px 6px 0px] bg-[#FFE58C] lg:mt-8">
      <div class="p-4 sm:mr-4 sm:ml-8 md:ml-12 lg:ml-16">
  <div class="productDetailTitle">{{ productData.title }}</div>
  <div class="productDetailContent">{{ productData.content }}</div>
  <div>
    <button class="productDetailBtn">
      Discover Product
    </button>
  </div>
</div>
     <div>
      <Accordion />
     </div>
    </div>
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