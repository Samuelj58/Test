<template>
  <div>
    <h1>Cart</h1>
    <div class="products">
      <div v-for="(console, index) in cartItems" :key="index">
        <h3>{{ console.name }}</h3>
        <img :src="console.img" />
        <div>{{ console.price }}</div>
        <button @click="removeItemFromCart(console)">Remove from cart</button>
      </div>
    </div>
  </div>
</template>

<script>

</script>

<style>
</style>
