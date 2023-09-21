<template>
    <div class="product-card__cart-btn" :class="isClicked ? 'clickFalse':'clickTrue'" 
        @click="cartClick"
        title="Добавить в корзину">
        <img v-if="isClicked == false" 
            src="../assets/cart-2.png" 
            alt="">
        {{ isClicked ? 'Отменить' : 'Купить' }}
    </div>
</template>

<script>
export default {
    name: 'cartBtn',
    props: {
        item: {
            type: Array,
            required: true
        }
    },
    data() {
        return {
            isClicked: false,
        }
    },
    methods: {
        cartClick() {
            this.isClicked = !this.isClicked

            if (this.isClicked) {
                this.$store.state.counter++
                console.log(this.item)

                this.$store.dispatch('addToCart', this.item);
            }
            else {
                this.$store.state.counter--
            }

        }
    }
}
</script>

<style>
.product-card__cart-btn {
    /* position: absolute;
    bottom: 10px;
    right: 10px; */
    cursor: pointer;
    user-select: none;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 30px;
    width: 82px;
    padding: 0 10px;
    border-radius: 8px;
    color: white;
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 12px;
}

.clickTrue {
    background-color: #7272ff;
    border: 1px solid #b1b1b1;
}

.clickFalse {
    background-color: #ce5652;
    border: 1px solid #d4d4d4;
}

.product-card__cart-btn:hover {
    /* background-color: #878fff; */
    border: 1px solid #ffd9ba;
    box-shadow: 0 0 10px #c7d6ff;
    transition: 0.2s;
}

.product-card__cart-btn img {
    height: 15px;
    width: 15px;
    margin-right: 5px;
}
</style>

