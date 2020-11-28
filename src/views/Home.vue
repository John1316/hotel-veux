<template>
  <div class="home">
    <HomeView />
  </div>
</template>

<script>
// @ is an alias to /src
import HomeView from "@/components/HomeView.vue";

export default {
  name: "Home",
  components: {
    HomeView
  }
};
</script>
