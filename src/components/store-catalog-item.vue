<template>
    <div class="product-card" v-for="items in $store.state.catalog" :key="items.id">
        <favoriteBtn style="user-select: none;"/>
        <!-- <div class="product-card__favorite-btn" title="Добавить в избранное">
            <img src="../assets/favorite.png" alt="">
        </div> -->
        <div class="product-card__img-block">
            <img :src="items.img" alt="">
        </div>
        <div class="product-card__info-block">
            <div class="product-card__title" :title="items.title">
                {{ sliceTitle(items.title) }}
            </div>
                <div v-if="items.discount">
                   <div class="">
                        <div class="product-card__discount" :title="items.price">
                            {{ slicePrice(items.price) }}
                        </div>
                   </div>
                    <div class="product-card__price-and-btn">
                        <div class="product-card__price product-card__price_discount" :title="items.discount" style="color: red;">
                            {{ slicePrice(items.discount) }}
                            <img src="../assets/discount.png" alt="">
                        </div>
                        <cartBtn :item="items"/>
                    </div>
                </div>

                <div v-else>
                    <div class="product-card__price-and-btn">
                        <div class="product-card__price" :title="items.price">
                            {{ slicePrice(items.price) }}
                        </div>
                        <cartBtn :item="items"/>
                    </div>
                </div>
        </div>
    </div>
</template>

<script>
import cartBtn from './cart-btn.vue'
import favoriteBtn from './favorite-btn.vue'

export default {
    name: 'storeCatalogItem',
    data() {
        return {
            counter: 0,
            isClicked: false
        }
    },
    // props: {
    //     catalog: {
    //         type: Array,
    //         default() {
    //             return []
    //         }
    //     }
    // },
    methods: {
        sliceTitle(elem) {
            if (elem.length > 70) {
                return elem.slice(0, 68) + '...'
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
        cartBtn,
        favoriteBtn
    }
}
</script>

<style>

.product-card {
    cursor: pointer;
    position: relative;
    /* display: flex;
    flex-direction: column;
    justify-content: space-between; */
    align-items: center;
    border: 1px solid #dbdbdb;
    box-shadow: 0 0 15px #d8d8d8;
    border-radius: 5px;
    width: 224px;
    max-height: 400px;
    margin-bottom: 10px;
    padding: 12px;
}

.product-card:not(:nth-child(4n)) {
    /* background-color: red; */
    margin-right: 12px;
}

.product-card:hover {
    box-shadow: 0 0 25px #cccccc;
    border: 1px solid #bebebe;
    transition: 0.2s;
}


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

.product-card__img-block {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 200px;
    max-width: 210px;
    margin-bottom: 12px;

}

.product-card__img-block img {
    max-height: 100%;
    max-width: 100%;
    cursor: pointer;
}

.product-card__info-block {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 120px;
    width: 100%;
}

.product-card__title {
    cursor: pointer;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 13px;
}

.product-card__title:hover {
    color: #8276ac;
    transition: 0.2s;
}

.product-card__price-and-btn {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.product-card__price {
    /* position: relative; */
    cursor: default;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.product-card__price_discount {
    display: inline-flex;
    /* align-items: center; */
    /* padding: 3px 6px 3px 3px;  
    background-color: white;
    border-radius: 25px;
    border: 1px solid #e6a4a4; */
    font-size: 15px;
}

.product-card__price_discount img {
    margin-left: 3px;
    width: 20px;
    height: 20px;
}

.product-card__discount {
    display: inline-flex;
    align-items: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    text-decoration: line-through;
    /* padding: 3px 3px 3px 6px;  
    background-color: white;
    border-radius: 25px;
    border: 1px solid #e6a4a4; */
    font-size: 12px;
}

/* .product-card__discount img {
    margin-left: 5px;
    width: 20px;
    height: 20px;
} */

/* .product-card__cart-btn {
    cursor: pointer;
    user-select: none;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 30px;
    padding: 0 10px;
    background-color: #7272ff;
    border: 1px solid #b1b1b1;
    border-radius: 8px;
    color: white;
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 12px;
}

.product-card__cart-btn:hover {
    background-color: #6c8eff;
    transition: 0.2s;
}

.product-card__cart-btn img {
    height: 15px;
    width: 15px;
    margin-right: 5px;
} */

</style>