<template>
  <header id="header" class="header">
    <div class="container">
      <div class="header-box">
        <a href="#/" class="header-logo logo">
          <img src="../assets/images/logo.png" alt="logo" />
        </a>
        <div class="header-controls">
          <button class="btn btn-primary">
            <img src="../assets/images/icons/user.png" alt="user" />
            Sign in
          </button>
          <button class="btn btn-outline" @click="openModal()">
            <img
              src="../assets/images/icons/shopping-cart.png"
              alt="shopping-cart"
            />
            Cart
          </button>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
const emit = defineEmits(["toggleModal"]);
const openModal = () => {
  emit("toggleModal");
  console.log("open");
};
</script>

<style scoped>
.header {
  min-height: 124px;
  display: flex;
  align-items: center;
}

.header-box {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-controls {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 10px;
}
</style>
