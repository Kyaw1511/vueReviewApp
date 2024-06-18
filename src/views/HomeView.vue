<template>
  <div class="home">
    <div class="container">
      <!-- Review Form -->
      <reviews-form />
      <!-- Review Stats --> 
      <review-status />
      <!-- Review List-->
      <review-list />
    </div>
  </div>
</template>
<script setup>
  import ReviewsForm from "../components/ReviewsForm.vue";
  import ReviewStatus from "../components/ReviewStatus.vue";
  import ReviewList from "../components/ReviewList.vue";
</script>
