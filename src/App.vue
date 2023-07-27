<template>
  <header-Uber-Eats />
  <main class="main-container">
    <input-Restaurant class="mt-5" />
    <h1 class="name-list-restaurant">Рестораны в Москве</h1>
    <div class="d-flex flex-wrap row">
      <restaurantItem
        v-for="restaurant in restaurants"
        :key="restaurant"
        class="col-lg-4 col-md-6 col-12"
      />
    </div>
  </main>
</template>

<script>
import headerUberEats from "./components/index-components/header-uber-eats";
import inputRestaurant from "./components/index-components/input-restaurant.vue";
import restaurantItem from "./components/index-components/restaurant-item.vue";
export default {
  components: {
    headerUberEats,
    inputRestaurant,
    restaurantItem,
  },
  data() {
    return {
      restaurants: [],
    };
  },
  created() {
    this.restaurants.push(1);
    this.restaurants.push(1);
    this.restaurants.push(1);
    this.restaurants.push(1);
    this.restaurants.push(1);
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=League+Spartan:wght@400;600&family=Roboto&display=swap");

.name-list-restaurant {
  margin-top: 55px;
  color: #1d1d1d;
  font-family: Roboto;
  font-size: 22px;
  font-style: normal;
  font-weight: 400;
  line-height: 34px;
}

@media (min-width: 1199px) {
  .main-container {
    margin-left: 80px;
    margin-right: 80px;
  }
}

@media (max-width: 1199px) {
  .main-container {
    margin-left: 8px;
    margin-right: 8px;
  }
}

.card-restaurant-container {
  margin-top: 20px;
}

.card-restaurant-container {
  margin-top: 20px;
}

.card-restaurant-description {
  margin-top: 15px;
  font-family: Roboto;
}

.name-restaurant {
  color: #1d1d1d;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
}

.cost-BaseProducts-restaurant {
  margin-top: 4px;
  color: #626262;
  font-size: 14px;
  font-weight: 400;
  line-height: 21px;
}

.cooking-time-restaurant {
  margin-top: 4px;
  color: #1d1d1d;
  font-size: 13px;
  font-weight: 400;
  line-height: 21px;
}
</style>
