<script setup>
import OrderSummary from './components/OrderSummary.vue'
</script>

<template>
  <OrderSummary msg="Vite + Vue" />
</template>

<style lang="scss">
body {
    background: hsl(225, 100%, 94%);
}

#app {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}
</style>
