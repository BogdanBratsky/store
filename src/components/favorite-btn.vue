<template>
    <div class="product-card__favorite-btn" title="Добавить в избранное" @click="this.isClicked = !this.isClicked">
        <img v-if="this.isClicked == false" src="../assets/favorited.png" alt="">
        <img v-if="this.isClicked == true" src="../assets/added.png" alt="">
    </div>
</template>

<script>
export default {
    name: 'favoriteBtn',
    data() {
        return {
            isClicked: false
        }
    },
    methods: {
        
    }
}
</script>

<style>
.product-card__favorite-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    position: absolute;
    top: 0;
    right: 0;
    width: 32px;
    height: 32px;
    background-color: white;
    margin: 9px 9px 0 0;
    border: 1px solid #dbdbdb;
    border-radius: 5px;
    box-shadow: 0 0 15px #cccccc;
}

.product-card__favorite-btn img {
    height: 18px;
    width: 18px;
}

.product-card__favorite-btn:hover img {
    scale: 1.15;
    transition: 0.5s;
}
</style>

