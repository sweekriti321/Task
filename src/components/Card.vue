<template>
  <div @click="discoverBtn" class="border border-gray-300 rounded-md lg:w-[266px] lg:h-[232px] sm:w-[342px] sm:h-[24px] sm:rounded-2xl sm:border-[0px] sm:border-[8px,0px]
">
    <div class="p-4">
      <div class="mb-2 flex justify-between">
        <div class="text-xl font-semibold leading-6 text-left">
          {{ cardData.title }}
        </div>
        <div>
          <img :src="require(`@/${cardData.src}`)" alt="Card Image" class="h-12 w-auto" />
        </div>
      </div>
      <div class="hidden lg:block">
        {{ cardData.content }}
      </div>
    </div>
    <div :class="{'bg-yellow-500 shadow-indigo-90 shadow-xl': isClicked, 'bg-stone-200': !isClicked }" class="w-[143.26px] h-[56px] p-[16px 24px] rounded-tl-[0px] rounded-tr-[50px] rounded-bl-[0px] rounded-br-[0px] border border-transparent hover:shadow-md hover:shadow-indigo-900 hover:bg-yellow-400 font-bold text-base cursor-pointer mt-10 hidden lg:block">
      <button class="mt-2 p-2" @click="discoverBtn">
        Discover
        <img :src="require('@/assets/downarrow.png')" class="float-end ml-6 mt-1" />
      </button>
    </div>
  </div>
</template>
  
  <script>
  export default {
    name: "cardView",
    props:{
        cardData:{
            type: Object,
            required: true
        },
        cardId: {
      type: Number,
      required: true
    },
    isClicked: {
      type: Boolean,
      required: true
    }
    },
    data() {
      return {
      };
    },
    methods:{
      discoverBtn(){
        this.$emit('productDetailDiscoverClick', this.cardId)
      }
    }
  };
  </script>