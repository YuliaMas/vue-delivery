<script setup>
import { ref, computed } from "vue";
import HomeView from "./views/HomeView.vue";
import ProductView from "./views/ProductView.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Modal from "./components/Modal.vue";

const isOpen = ref(false);

const routes = {
  "/": HomeView,
  "/rest": ProductView,
};

const currentPath = ref(window.location.hash);

window.addEventListener("hashchange", () => {
  currentPath.value = window.location.hash;
});

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || "/"] || NotFound;
});
</script>

<template>
  <div class="page-wrapper">
    <a href="#/">HomeView</a>
    <a href="#/rest">ProductView</a>
    <Header @toggleModal="isOpen = !isOpen" />
    <main id="main" class="main">
      <!-- <router-view></router-view> -->
      <component :is="currentView" />
    </main>
    <Modal :isOpen="isOpen" @toggleModal="isOpen = !isOpen" />
    <Footer />
  </div>
</template>

<style scoped></style>
