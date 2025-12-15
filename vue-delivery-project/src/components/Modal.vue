<script setup>
const { isOpen } = defineProps({ isOpen: Boolean });
console.log(isOpen);
const emit = defineEmits(["toggleModal"]);
const closeModal = () => emit("toggleModal");
</script>
props

<template>
  <div
    class="cart-modal__overlay"
    :class="{ open: isOpen }"
    @click.self="closeModal()"
  >
    <div class="cart-modal">
      <div class="cart-modal__header">
        <h2 class="cart-modal__header--title">Shopping cart</h2>
        <span class="cart-modal__header--close" @click="closeModal()">
          <img src="../assets/images/icons/close.svg" alt="close" />
        </span>
      </div>

      <div class="cart-modal__body">
        <div class="cart-item">
          <p class="cart-item__title">Roll eel standard</p>
          <div class="cart-item__controls">
            <div class="cart-items__controls--price">2.50 $</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-items__controls__count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>
        <div class="cart-item">
          <p class="cart-item__title">Roll eel standard</p>
          <div class="cart-item__controls">
            <div class="cart-items__controls--price">2.50 $</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-items__controls__count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>
        <div class="cart-item">
          <p class="cart-item__title">Roll eel standard</p>
          <div class="cart-item__controls">
            <div class="cart-items__controls--price">2.50 $</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-items__controls__count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>
        <div class="cart-item">
          <p class="cart-item__title">Roll eel standard</p>
          <div class="cart-item__controls">
            <div class="cart-items__controls--price">2.50 $</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-items__controls__count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>
        <div class="cart-item">
          <p class="cart-item__title">Roll eel standard</p>
          <div class="cart-item__controls">
            <div class="cart-items__controls--price">2.50 $</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-items__controls__count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>
      </div>

      <div class="cart-modal__footer">
        <div class="cart-modal__footer--price">12.50 $</div>
        <div class="cart-modal__footer--controls">
          <button class="btn btn-primary">Checkout</button>
          <button class="btn btn-outline">Cancel</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cart-modal__overlay {
  display: none;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  /* background: #00000066; */
  background: rgba(0, 0, 0, 0.4);
  align-items: center;
  justify-content: center;
}

.cart-modal__overlay.open {
  display: flex;
}

.cart-modal {
  width: 100%;
  max-width: 780px;
  padding: 40px 45px;
  border-radius: 5px;
  background: #fff;
}

.cart-modal__header--title {
  font-weight: 700;
  font-size: 36px;
  line-height: 100%;
  color: #000;
  margin: 0;
}

.cart-modal__header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 48px;
}

.cart-modal__header--close {
  cursor: pointer;
}

.cart-modal__footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 50px;
}

.cart-modal__footer--price {
  opacity: 1;
  border-radius: 5px;
  padding: 15px 20px;
  background: #262626;
  font-weight: 700;
  font-size: 20px;
  line-height: 100%;
  color: #fafafa;
}

.cart-modal__footer--controls {
  display: flex;
  align-items: center;
  gap: 10px;
}

.cart-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
}

.cart-item:not(:last-child) {
  padding-bottom: 10px;
  margin-bottom: 10px;
  border-bottom: 1px solid #d9d9d9;
}

.cart-item__title {
  font-weight: 400;
  font-size: 18px;
  line-height: 32px;
  color: #000000;
  margin: 0;
}

.cart-item__controls {
  display: flex;
  align-items: center;
}

.cart-items__controls--price {
  margin-right: 48px;
  font-weight: 700;
  font-size: 20px;
  line-height: 32px;
}

.cart-item__controls button {
  border: 1px solid #40a9ff;
  color: #40a9ff;
}

.cart-items__controls__count {
  margin: 0 16px;
}
</style>
