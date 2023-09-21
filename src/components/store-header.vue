<template>
        <header class="header">
            <nav class="header__nav">
                <div class="header__logo-search-block">
                    <div class="header__logo">
                        <!-- <img src="../assets/logo.png" alt=""> -->
                        STORE
                    </div>
                    <storeSearch/>
                </div>
                <div class="header__favorite-and-cart">
                    <storeFavorite/>
                    <!-- <cartCounter/> -->
                    <storeCart/>
                </div>
            </nav>
        </header>
</template>

<script>
import storeSearch from './store-search.vue';
import storeCart from './store-cart.vue';
import storeFavorite from './store-favorite.vue';
// import cartCounter from './cart-counter.vue';

export default {
    name: 'storeHeader',
    data() {
        return {
        }
    },
    components: {
        storeSearch,
        storeCart,
        storeFavorite,
        // cartCounter
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap');

.header {
    background-color: white;
    position: fixed;
    top: 0;
    user-select: none;
    width: 100%;
    /* background-color: #fff1ec; */
    border-bottom: 1px solid #e6e6e6;
    box-shadow: 0 1px 5px #ececec;
    z-index: 9999;
}

.header__nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin: 0 auto;
    width: 1170px;
    height: 54px;
}

.header__logo-search-block {
    display: flex;
    align-items: center;
    /* justify-content: space-between; */
    /* width: 300px; */
}

.header__logo {
    /* #7c7cc7
    #d65454 */
    font-family: 'Fredoka One', cursive;
    cursor: pointer;
    color: #666666;
    font-size: 26px;
    /* margin-bottom: 4px; */
    /* text-shadow: 2px 2px 1px #bebebe; */
    margin-right: 20px;
    /* margin-bottom: 5px; */
}

.header__favorite-and-cart {
    position: relative;
    display: flex;
    align-items: center;
}

</style>