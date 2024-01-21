<template>
  <div class="lg:w-[1103px] lg:h-[744px] lg:gap-40 text-black lg:m-8  lg:-left-9 lg:top-155 sm:w-[Hug_(347px)] sm:h-[Hug_(1,236px)] sm:gap-6">
    <div class="mb-2">
      <h1 class="head_text text-center">
        Section Title
        <br class="max-md:hidden" />
        <span class="head_subtitle text-center">
          Section Subtitle
        </span>
      </h1>
    </div>
    <ProductView />
  </div>
</template>

<script>
import ProductView from './productView.vue';

export default{
    name: "pageView",
    components: { ProductView }
}
</script>