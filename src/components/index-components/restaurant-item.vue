<template>
  <div>
    <img :src="restaurant.urlImg" class="card-img-top" :alt="restaurant.name" />
    <div class="card-restaurant-description">
      <div class="name-restaurant">{{ restaurant.name }}</div>
      <div class="cost-BaseProducts-restaurant">
        {{ restaurant.costBaseProducts }}
      </div>
      <div class="cooking-time-restaurant">
        {{ restaurant.cookingTime }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    restaurant: {
      type: Object,
      required: true,
      default: null,
    },
  },
};
</script>

<style>
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
