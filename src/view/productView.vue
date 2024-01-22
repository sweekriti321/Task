<template>
  <div>
  <div class="flex flex-wrap justify-center sm:justify-start gap-4">
  <div v-for="(card, index) in cardItems" :key="index">
  <Card
  :cardData="card"
  @productDetailDiscoverClick="showProductDetail(card.cardId)"
  :isClicked="card.cardId === expandProductDetail"
  />
  </div>
  </div>
  
  <ProductDetail
  v-if="expandProductDetail !== null"
  :productData="productItems[expandProductDetail]"
  />
  </div>
  </template>
  
  <script>
  import Card from "@/components/Card.vue";
  import ProductDetail from "@/components/ProductDetail.vue";
  
  export default {
  name: "productView",
  components: {
  Card,
  ProductDetail,
  },
  data() {
  return {
  expandProductDetail: 1,
  cardItems: [
  {
  cardId: 1,
  title: "Birthday Gifts",
  src: "assets/firstcard.png",
  content: "Here you can find different types of birthday gifts to gift your loved ones. Celebrate with happiness.",
  },
  {
  cardId: 2,
  title: "Anniversary Gifts",
  src: "assets/secondcard.png",
  content:
  "Here you can find different types of anniversary gifts to gift your loved ones. Celebrate with happiness."  },
  {
  cardId: 3,
  title: "Graduation Gifts",
  src: "assets/thirdcard.png",
  content:
  "Here you can find different types of graduation gifts to gift your loved ones. Celebrate with happiness.",
  },
  {
  cardId: 4,
  title: "Gifts for Married couple",
  src: "assets/fourthcard.png",
  content: "Here you can find different types of gifts to gift your married couple friends and family. Celebrate with happiness.",
  },
  ],
  productItems: {
  1: {
  title: "Different types of Birthday Gift",
  content:
  "Here you can find different types of birthday gifts to gift your loved ones.",
  },
  2: {
  title: "Different types of Anniversary Gift",
  content: "Here you can find different types of anniversary gifts to gift your loved ones.",
  },
  3: {
  title: "Gifts for graduation",
  content: "Here you can find different types of graduation gifts to gift your loved ones.",
  },
  4: {
  title: "Gifts for Married Couple",
  content: "Here you can find different types of birthday gifts to gift your loved ones.",
  },
  },
  };
  },
  
  methods: {
  showProductDetail(cardId) {
  this.expandProductDetail = cardId;
  },
  },
  };
  </script>