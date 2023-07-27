<template>
  <header-Uber-Eats />
  <main class="main-container">
    <input-Restaurant class="mt-5" />
  </main>
</template>

<script>
import headerUberEats from "./components/index-components/header-uber-eats";
import inputRestaurant from "./components/index-components/input-restaurant.vue";
export default {
  components: {
    headerUberEats,
    inputRestaurant,
  },
};
</script>

<style>
.main-container {
  margin-left: 60px;
  margin-right: 60px;
}
</style>
