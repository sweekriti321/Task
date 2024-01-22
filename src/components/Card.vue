<template>
  <div
  @click="discoverBtn"
  class="border-b-4 border-b-yellow-500 border-2 border-gray-300 rounded-xl w-[266px] sm:border-b-gray-300"
  >
  <div class="flex flex-col items-center m-4">
  <div class="flex w-full mb-2 sm:flex-row gap-2 sm:justify-between">
  <span
  class="text-xl break-all font-semibold leading-6 order-last sm:order-first"
  >
  {{ cardData.title }}
  </span>
  <img
  :src="require(`@/${cardData.src}`)"
  alt="Card Image"
  class="h-12 w-auto order-first object-left sm:order-last"
  />
  </div>
  <div class="my-2 w-full hidden sm:block text-wrap break-all line-clamp-3">
  {{ cardData.content }}
  </div>
  </div>
  <div
  :class="{
  'bg-yellow-500 shadow-indigo-90 shadow-xl': isClicked,
  'bg-stone-200': !isClicked,
  }"
  class="hidden sm:block w-[143.26px] h-[56px] p-[16px 24px] rounded-tl-[0px] rounded-tr-[50px] rounded-bl-lg rounded-br-[0px] border border-transparent hover:shadow-md hover:shadow-indigo-900 hover:bg-yellow-400 font-bold text-base cursor-pointer"
  >
  <button class="mt-2 p-2" @click="discoverBtn">
  Discover
  <img
  :src="require('@/assets/downarrow.png')"
  class="float-end ml-6 mt-1"
  />
  </button>
  </div>
  </div>
  </template>
  
  <script>
  export default {
  name: "cardView",
  props: {
  cardData: {
  type: Object,
  required: true,
  },
  cardId: {
  type: Number,
  required: true,
  },
  isClicked: {
  type: Boolean,
  required: true,
  },
  },
  data() {
  return {};
  },
  methods: {
  discoverBtn() {
  this.$emit("productDetailDiscoverClick", this.cardId);
  },
  },
  };
  </script>