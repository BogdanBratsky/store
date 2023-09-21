<template>
    <div class="searh-block">
        <input class="search-block__input" type="text" placeholder="Поиск">
        <button class="search-block__btn">
            <img src="../assets/search.png" alt="">
        </button>
    </div>
</template>

<script>
    export default {
        name: 'storeSearch'
    }
</script>

<style>

.searh-block {
    display: flex;
    height: 34px;
    width: 220px;
    border: 1px solid #e6e6e6;
    border-radius: 18px;
    padding: 2px;
}

.searh-block:focus-within {
    box-shadow: 0 0 15px #e9f3ff;
    border: 1px solid #e4e4f3;
}

.search-block__input {
    width: 185px;
    outline: none;
    border: none;
    background-color: transparent;
    border-radius: 50px;
    padding: 0 10px;
}

.search-block__input::placeholder {
    font-size: 12px;
}

.search-block__btn {
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: transparent;
    border: none;
    border-radius: 50px;
    height: 100%;
    width: 35px;
}

.search-block__btn img {
    height: 16px;
    width: 16px;
}

.search-block__btn:hover {
    background-color: #f6f6f8;
    transition: 0.2s;
}

</style>