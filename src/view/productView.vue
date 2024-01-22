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
  title: "Card Title",
  src: "assets/firstcard.png",
  content: "Lorem ipsum dolor sit amet, consect ksjflksdjflkgjhjkhgfhjkhgfdkasdjflsldfj sadlfjsalkdfjklasdfjlkasdf dipiscing elit.",
  },
  {
  cardId: 2,
  title: "Card Title for card 2",
  src: "assets/secondcard.png",
  content:
  "Lorem ipsum dolor sit amet, consect ksjflksdjflkgjhjkhgfhjkhgfdkasdjflsldfj sadlfjsalkdfjklasdfjlkasdf dipiscing elit.",
  },
  {
  cardId: 3,
  title: "Card Title for 3rd card",
  src: "assets/thirdcard.png",
  content:
  "Lorem ipsum dolor sit amet, consect ksjflksdjflkgjhjkhgfhjkhgfdkasdjflsldfj sadlfjsalkdfjklasdfjlkasdf dipiscing elit.",
  },
  {
  cardId: 4,
  title: "Card Title of 4th card",
  src: "assets/fourthcard.png",
  content: "Lorem ipsum dolor sit amet, consect ksjflksdjflkgjhjkhgfhjkhgfdkasdjflsldfj sadlfjsalkdfjklasdfjlkasdf dipiscing elit.",
  },
  ],
  productItems: {
  1: {
  title: "Product Title",
  content:
  "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent scelerisque risus id ante maximus blandit.",
  },
  2: {
  title: "Product Title 2",
  content: "This is product 2.",
  },
  3: {
  title: "Product Title 3",
  content: "This is product 3.",
  },
  4: {
  title: "Product Title 4",
  content: "This is product 4.",
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