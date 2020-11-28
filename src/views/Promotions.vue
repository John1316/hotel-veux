<template>
  <div class="about">
    <PromotionsDetails />
  </div>
</template>

<script>
// @ is an alias to /src
import PromotionsDetails from "@/components/PromotionsDetails.vue";

export default {
  name: "Promotion",
  components: {
    PromotionsDetails
  }
};
</script>
