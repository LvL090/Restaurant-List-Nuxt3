<script setup lang="ts">
import restaurants from "@/data.json";

const route = useRoute();
const name = route.params.name;

const restaurant = restaurants.find((r) => r.name === name);
</script>

<template>
  <NuxtLayout name="custom" v-if="restaurant">
    <div class="restaurant-container">
      <div class="image-container">
        <nuxt-img
          :src="restaurant.imageUrl"
          sizes="sm:200px md:400px lg:800px"
          loading="lazy"
          width="1024"
          height="800"
          quality="75"
        />
      </div>
      <div class="info-container">
        <h1>{{ restaurant.name }}</h1>
        <div class="stats-container">
          <h5>Revenue (in billions)</h5>
          <p>{{ restaurant.revenue }}€</p>
        </div>
        <div class="stats-container">
          <h5>Number of Stores</h5>
          <p>{{ restaurant.numberOfStores }}</p>
        </div>
        <p class="content">{{ restaurant.content }}</p>
      </div>
    </div>
  </NuxtLayout>
</template>

<style scoped>
.restaurant-container {
  display: flex;
}
.image-container {
  margin: 1rem;
  width: 80%;
  height: 95vh;
}
.image-container img {
  width: 90%;
  height: 90%;
}
.restaurant-not-found {
  height: 75vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.info-container {
  padding: 3rem;
  width: 50%;
}
.info-container h1 {
  text-transform: uppercase;
  font-size: 6rem;
  margin-bottom: 3rem;
}
.stats-container {
  display: flex;
  align-items: flex-end;
  margin-bottom: 1rem;
}
.stats-container h5 {
  width: 20rem;
  font-size: 2rem;
  margin: 0;
  margin-right: 5rem;
}
.stats-container p {
  font-size: 2rem;
  margin: 0;
}
.content {
  font-size: 1.2rem;
  margin-top: 4rem;
}
</style>
