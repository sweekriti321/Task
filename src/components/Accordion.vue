<template>
  <div>
    <div v-for="(item, index) in accordionItems" :key="index" class="w-[Fixed_(421px)] h-[Hug_(56px)] pl-0 pr-[0px,] pt-[0px,] pb-[24px,]  border-black;
justify-space-between">
      <div
        @click="toggleAccordion(index)"
        class=" p-3 cursor-pointer flex items-center justify-between"
      >
      <img :src="require(`@/${item.src}`)" class="mr-6"/>
        <span class="font-semibold">{{ item.title }}</span>
        <img :src="require('@/assets/accordionicon.png')" class="float-end ml-6 mt-1"/>
      </div>
      <hr class="border-t-1 border-black"/>
      
      <div v-show="isOpen(index)" class="bg-white p-3 w-421 h-376">
        {{ item.content }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:"accordionTab",
  data() {
    return {
      accordionItems: [
        {src:'assets/group1.png', title: 'Accordion Item 1', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.' },
        {src:'assets/group2.png', title: 'Accordion Item 2', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.' },
        {src:'assets/group1.png', title: 'Accordion Item 3', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.' },
        {src:'assets/group3.png', title: 'Accordion Item 4', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.' },
        {src:'assets/group2.png', title: 'Accordion Item 5', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.' },
      ],
      openIndex: null,
    };
  },
  methods: {
    toggleAccordion(index) {
      if (this.isOpen(index)) {
        this.openIndex = null;
      } else {
        this.openIndex = index;
      }
    },
    isOpen(index) {
      return this.openIndex === index;
    },
  },
};
</script>