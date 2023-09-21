<template>
    <div class="sidebar">
        <header class="sidebar__title">Категории</header>
        <ul class="sidebar__list">
            <li class="sidebar__item">
                <img src="../assets/smartphones.png" alt="">
                Смартфоны
            </li>
            <li class="sidebar__item">
                <img src="../assets/books.png" alt="">
                Книги
            </li>
            <li class="sidebar__item">
                <img src="../assets/piano.png" alt="">
                Музыкальные инструменты
            </li>
            <li class="sidebar__item">
                <img src="../assets/games.png" alt="">
                Игровые консоли
            </li>
            <li class="sidebar__item">
                <img src="../assets/tv.png" alt="">
                Телевизоры
            </li>
            <li class="sidebar__item">
                <img src="../assets/studio.png" alt="" style="width: 18px; height: 18px; margin-right: 6px;">
                Студийное оборудование
            </li>
            <li class="sidebar__item">
                <img src="../assets/office.png" alt="">
                Офис
            </li>
            <li class="sidebar__item">
                <img src="../assets/gpu.png" alt="" style="width: 18px; height: 18px; margin-right: 6px;">
                Комплектующие для пк
            </li>
            <li class="sidebar__item">
                <img src="../assets/tools.png" alt="">
                Инструменты
            </li>
            <li class="sidebar__item">
                <img src="../assets/btech.png" alt="">
                Бытовая техника
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'storeSidebar',
        data() {
            return {

            }
        }
    }
</script>

<style>
/* ШРИФТЫ ДЛЯ КАТЕГОРИЙ */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');
/* ШРИФТЫ ДЛЯ ЗАГОЛОВКА */
@import url('https://fonts.googleapis.com/css2?family=Didact+Gothic&display=swap');

.sidebar {
    position: sticky;
    top: 66px;
    cursor: pointer;
    width: 224px;
    background-color: white;
    border: 1px solid #e9e9e9;
    box-shadow: 0 0 15px #f0f0f0;
    border-radius: 4px;
    font-family: 'Jost', sans-serif;
    font-size: 14px;
    margin-bottom: 10px;
}

.sidebar__title {
    user-select: none;
    height: 40px;
    border-bottom: 1px solid #e9e9e9;
    background-color: #fafafa;
    display: flex;
    align-items: center;
    /* justify-content: center; */
    padding: 0 10px;
    padding-bottom: 4px;
    font-size: 20px;
    border-radius: 5px 5px 0 0;
    font-family: 'Didact Gothic', sans-serif;
}

.sidebar__item {
    padding: 10px;
    display: flex;
    align-items: center;
}

.sidebar__item:hover {
    background-color: #f7f7f7;
    border-radius: 4px;
    transition: 0.2s;
}

.sidebar__item img {
    margin-right: 8px;
    width: 16px;
    height: 16px;
}

/* .sidebar li:last-child:hover {
    border-radius: 0 0 10px 10px;
}

.sidebar li:first-child:hover {
    border-radius: 0 0 10px 10px;
} */

</style>