<template>
    <div>
        <!-- <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4"> -->
         <div class="flex flex-wrap lg:space-x-4"> 
    <div v-for="(card,index) in cardItems" :key="index" class=" rounded-md w-full md:w-[266px]">
        <Card :cardData="card" @productDetailDiscoverClick="showProductDetail(card.cardId)" :isClicked="card.cardId === expandProductDetail"  />
    </div>
</div>
<div>
    <ProductDetail v-if="expandProductDetail !== null" :productData="this.productItems[expandProductDetail]"/>
  </div>
</div>
</template>
<script>
import Card from "@/components/Card.vue";
import ProductDetail from "@/components/ProductDetail.vue";

export default {
  name: "productView",
  components: {
    Card,
    ProductDetail
  },
  data() {
      return {
        expandProductDetail:1,
        cardItems: [
          {cardId:1, title: "Card Title", src: "assets/firstcard.png", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit." },
          {cardId:2, title: "Card Title 2 ok ok ok ok ok", src: "assets/secondcard.png", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit." },
          {cardId:3, title: "Card Title 3 ok", src: "assets/thirdcard.png", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit." },
          {cardId:4,title: "Card Title 4 ok", src: "assets/fourthcard.png", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit." }
        ],
        productItems:{
            1: {
              title: "Product Title",
              content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent scelerisque risus id ante maximus blandit."  
            },
            2: {
                title: "Product Title 2",
              content: "THis is product 2." 
            },
            3: {
                title: "Product Title 3",
              content: "THis is product 3." 
            },
            4: {
                title: "Product Title 4",
              content: "THis is product 4." 
            }
        }
      }
    },

    methods: {
        showProductDetail(cardId) {
            this.expandProductDetail = cardId
        
        }
    }
};
</script>