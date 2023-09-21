<template>
    <div class="up-btn" @click="pageUp">
        <img src="../assets/up.png" alt="">
    </div>
</template>

<script>
export default {
    name: 'upBtn',
    methods: {
        pageUp() {
            window.scrollTo(0, -5000)
        }
    }
}
</script>

<style>
.up-btn {
    cursor: pointer;
    /* position: sticky;
    right: 0;
    bottom: 0; */
    position: fixed;
    right: 10px;
    bottom: 10px;
    /* margin: 10px; */
    display: flex;
    align-items: center;
    justify-content: center;
    height: 30px;
    width: 30px;
    border: 1px solid #c9c9c9;
    border-radius: 3px;
    background-color: white;
}

.up-btn img {
    width: 18px;
    height: 18px;
}
</style>