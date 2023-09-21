<template>
    <div v-if="$store.state.counter > 0" class="cart-counter">{{ $store.state.counter }}</div>
</template>

<script>
export default {
    name: 'cartCounter'
}
</script>

<style>
.cart-counter {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 5px;
    padding: 0 6px;
    height: 20px;
    /* width: 20px; */
    background-color: #ffffff;
    border: 1px solid #a34a4a;
    border-radius: 50px;
    color: #000000;
    font-size: 13px;
    box-shadow: 0 0 6px #ffe796;
}
</style>