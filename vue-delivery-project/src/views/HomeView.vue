<template>
  <section class="banner">
    <div class="container">
      <div class="banner-item">
        <h2 class="banner-item--title">
          Order food <br />
          delivery to your home
        </h2>
        <p class="banner-item--subtitle">
          The courier will deliver food from your favorite restaurant, wearing
          gloves, a mask, and carrying hand sanitizer.
        </p>
      </div>
    </div>
  </section>

  <section class="products">
    <div class="container">
      <div class="products-header">
        <h3 class="products-header--title">Restaurants</h3>
        <input
          type="text"
          name="search"
          class="products-header--search"
          placeholder="Search for dishes and restaurants"
        />
      </div>

      <div class="products-wrapper" id="rests-container">
        <router-link
          class="products-card"
          v-for="rest in restArray"
          :key="rest.id"
          :to="`/rest?id=${rest.id}`"
        >
          <div class="products-card__image">
            <img :src="getUrl(rest.image)" alt="{{ rest.title }}" />
          </div>
          <div class="products-card__description">
            <div class="products-card__description-row">
              <h4 class="products-card__description--title">
                {{ rest.title }}
              </h4>
              <div class="products-card__description--badge">
                {{ rest.time }} min
              </div>
            </div>
            <div class="products-card__description-row">
              <div class="products-card__description-info">
                <div class="products-card__description-info--raiting">
                  <img src="../assets/images/icons/star.svg" alt="star" />
                  {{ rest.rating }}
                </div>
                <div class="products-card__description-info--price">
                  From {{ rest.price }} $
                </div>
                <div class="products-card__description-info--group">
                  {{ rest.type }}
                </div>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </section>
</template>

<script setup>
import { restArray } from "@/constants/rests";
const getUrl = (name) => {
  return new URL(`../assets/images/rests/${name}`, import.meta.url);
};
</script>
