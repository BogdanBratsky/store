<template>
    <div class="header__favorite-block">
        Избранное
        <img src="../assets/header-favorite.png" alt="">
    </div>
</template>

<script>
    export default {
        name: 'storeFavorite'
    }
</script>
    
<style>

.header__favorite-block {
    user-select: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    margin-right: 10px;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-size: 12px;
    padding: 6px 10px;
    border-radius: 50px;
    border: 1px solid #ececec;
    color: #505050;
    background-color: #fafafa;
}

.header__favorite-block img {
    margin-left: 6px;
    width: 20px;
    height: 20px;
}

.header__favorite-block:hover {
    background-color: #f1f1f1;
    transition: 0.2s;
}

.header__favorite-block:active {
    background-color: #ffffff;
    border: 1px solid #ffe3e3;
    color: #c77777;
    /* transition: 0.2s; */
}

</style>