<template>
    <div class="cart-block" @click="showPopup">
        <img src="../assets/cart-2.png" alt="">

        <div v-if="isVisible" class="cart-block__popup" @click.stop>
            <header class="cart-block__header">
                <div class="cart-block__title">Корзина</div>
                <!-- <div class="cart-block__product-counter">{{ $store.state.counter }}</div> -->
                <div class="cart-block__close-btn" @click="closePopup">&times;</div>
            </header>

            <div style="max-height: 450px; overflow-y: auto;">
                <div class="cart-block__items" v-for="items in $store.state.cartStorage" :key="items.id">
                    <div class="cart-block__item">
                        <div class="item__image-block">
                            <img :src="items.img" alt="">
                        </div>
                        <div class="item__info-block">
                            <div class="item__title" :title="items.title">{{ sliceTitle(items.title) }}</div>
                            <div class="item__price" :title="items.price">{{ slicePrice(items.price) }}</div>
                        </div>
                    </div>
                </div>
            </div>

            <footer class="cart-block__info">
                <div class="info__total-price">Итого: </div>
            </footer>
        </div>

        <cartCounter style="position: absolute; bottom: 30%; right: 65%;"/>
    </div>
</template>

<script>
import cartCounter from './cart-counter.vue';

export default {
    name: 'storeCart',
    data() {
        return {
            isVisible: true
        }
    },
    methods: {
        showPopup() {
            this.isVisible = !this.isVisible;
        },
        closePopup() {
            this.isVisible = false;
        },
        sliceTitle(elem) {
            if (elem.length > 60) {
                return elem.slice(0, 58) + '...'
            }
            return elem
        },
        slicePrice(elem) {
            if (elem.length > 10) {
                return elem.slice(0, 8) + '...р.'
            }
            return elem
        },
    },
    components: {
        cartCounter
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Didact+Gothic&display=swap');

.cart-block__popup {
    cursor: default;
    position: absolute;
    top: 100%;
    right: 0;
    width: 380px;
    background-color: #ffffff;
    border: 1px solid #e6e6e6;
    border-radius: 9px;
    /* box-shadow: 0 10px 30px #dfdfdf; */
    margin-top: 2px;
    /* padding: 0 10px; */
}

.cart-block__header {
    display: flex;
    /* justify-content: center; */
    align-items: center;
    justify-content: space-between;
    height: 45px;
    border-bottom: 1px solid #f0f0f0;
    font-size: 20px;
    font-family: 'Didact Gothic', sans-serif;
    padding: 0 10px;
}

.cart-block__close-btn {
    /* display: flex;
    align-items: center;
    height: 100%; */
    cursor: pointer;
    font-size: 40px;
    color: grey;
    padding-bottom: 5px;
}

.cart-block__items {
    display: flex;
    flex-direction: column;
}

.cart-block__item {
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 10px;
    height: 100px;
}

.cart-block__item:hover {
    background-color: #fafafa;
    border-radius: 10px;
}

.cart-block__item:not(:last-child) {
    border-top: 1px solid #000000;
}

.cart-block__item:hover {
    color: #8276ac;
    transition: 0.2s;
}

.cart-block__item:hover img {
    box-shadow: 0 0 10px #e6e6e6;
    transition: 0.2s;
}

.cart-block__item:hover .item__title {
    text-shadow: 0 0 10px #d2c0e0;
}

.item__image-block {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: white;
    border-radius: 8px;
    height: 70px;
    width: 70px;
}

.item__image-block img {
    /* display: flex; */
    border-radius: 7px;
    min-width: 100%;
    min-height: 100%;
    object-fit: contain;
    /* flex: 1; */
}

.item__info-block {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 270px;
    height: 100%;
    padding-left: 10px;
}

.item__title {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 13px;
}

.item__price {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 13px;
    margin-bottom: 10px;
    color: #4d4d4d;
}

.cart-block__info {
    display: flex;
    align-items: center;
    border-top: 1px solid #f0f0f0;
    height: 45px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    padding: 0 10px;
}

.cart-block {
    position: relative;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 32px;
    width: 58px;
    border: 1px solid #b1b1b1;
    border-radius: 6px;
    background-color: #7272ff;
}

.cart-block:hover {
    background-color: #6c8eff;
    transition: 0.2s;
}

.cart-block img {
    margin-left: 2px;
    width: 20px;
    height: 20px;
}

</style>