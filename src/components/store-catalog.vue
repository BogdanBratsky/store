<template>
    <main class="main">
        <div class="main__wrapper">
            <div class="">
                <storeSidebar/>
            </div>
            <div class="main__products">
                <storeCatalogItem/>
                <!-- <div class="pagination">
                    <div class="pagination__item"></div>
                </div> -->
            </div>
        </div>
    </main>
</template>

<script>
    import storeCatalogItem from './store-catalog-item.vue';
    import storeSidebar from './store-sidebar.vue';

    export default {
        name: 'storeCatalog',
        data() {
            return {
                // catalog: [
                //     {
                //         id: 0,
                //         title: 'Смартфон Apple iPhone 11 128 ГБ черный',
                //         price: '49 999 р.',
                //         discount: '39 990 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/9951aa6a99611e4df95c83529680ba0f/c73bba26affbf44a01db51117e576f246bfd88a6402b11546368887a7f8ad707.jpg.webp',
                //     },
                //     {
                //         id: 1,
                //         title: 'KEPMA D1C Natural Matt',
                //         price: '13 700 р.',
                //         img: 'https://www.muztorg.ru/files/62d/13q/ei8/o00/c08/s4g/ww8/wkw/62d13qei8o00c08s4gww8wkw0.jpg',
                //     },
                //     {
                //         id: 2,
                //         title: '65" (163 см) Телевизор LED Xiaomi Mi TV 4S 65 серебристый',
                //         price: '59 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/7377b6b9fcdd0e463d55bd619eb6ee42/b9b8b99f9430272de6288608c0323a5743e452bcdc485e0ad7bb436648fe7e14.jpg.webp',
                //     },
                //     {
                //         id: 3,
                //         title: 'Игровая консоль PlayStation 4 Slim',
                //         price: '44 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/2e00de8b4786143bcdfb6f8a5edbcc62/23ef531b89e6e0608e5ad56c97bf6fef5ef5f497ee9f4c6276e995ef2d00c494.jpg.webp',
                //     },
                //     {
                //         id: 4,
                //         title: 'Игровая консоль PlayStation 5 Digital Edition',
                //         price: '49 299 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/976d9d4a3edb4dd5b74ef33477d52508/12135f5e78851059c0aa25212425cbee8437d03a9dcb71a3ed31c64920b750ce.jpg.webp',
                //     },
                //     {
                //         id: 5,
                //         title: 'Сочинения в прозе. Александр Пушкин',
                //         price: '8 778 р.',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/27/226/2722620.jpg',
                //     },
                //     {
                //         id: 6,
                //         title: 'Yamaha MONTAGE6t',
                //         price: '444 000 р.',
                //         img: 'https://www.muztorg.ru/files/biw/5f8/bhf/koc/ook/wwk/s4k/s8c/o/biw5f8bhfkocookwwks4ks8co.jpg',
                //     },
                //     {
                //         id: 7,
                //         title: 'FOCUSRITE Scarlett 18i20 3rd Gen',
                //         price: '72 400 р.',
                //         img: 'https://www.muztorg.ru/files/36z/b26/pwb/fi8/cgs/4cw/g4w/kso/o/36zb26pwbfi8cgs4cwg4wksoo.jpg',
                //     },
                //     {
                //         id: 8,
                //         title: 'История государства Российского.Юбилейное издание.2 кн.',
                //         discount: '2 922 ₽',
                //         price: '3 299 ₽',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/25/726/2572693.jpg',
                //     },
                //     {
                //         id: 9,
                //         title: 'Принтер струйный Canon PIXMA G1420 [цветная печать, A4, 4800x1200 dpi, ч/б - 9.1 стр/мин (А4), USB-B, СНПЧ]',
                //         price: '17 499 ₽',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/200/200/066e011bff305be3ecb2a0532adb44c1/5966091faeca3adb3bd7b0d460a58662d08c7ed30a0c57ea697fd20de2d0d5e9.jpg.webp',
                //     },
                //     {
                //         id: 10,
                //         title: 'Смартфон Apple iPhone 11 128 ГБ черный',
                //         price: '49 999 р.',
                //         discount: '39 990 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/9951aa6a99611e4df95c83529680ba0f/c73bba26affbf44a01db51117e576f246bfd88a6402b11546368887a7f8ad707.jpg.webp',
                //     },
                //     {
                //         id: 11,
                //         title: 'KEPMA D1C Natural Matt',
                //         price: '13 700 р.',
                //         img: 'https://www.muztorg.ru/files/62d/13q/ei8/o00/c08/s4g/ww8/wkw/62d13qei8o00c08s4gww8wkw0.jpg',
                //     },
                //     {
                //         id: 12,
                //         title: '65" (163 см) Телевизор LED Xiaomi Mi TV 4S 65 серебристый',
                //         price: '59 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/7377b6b9fcdd0e463d55bd619eb6ee42/b9b8b99f9430272de6288608c0323a5743e452bcdc485e0ad7bb436648fe7e14.jpg.webp',
                //     },
                //     {
                //         id: 13,
                //         title: 'Игровая консоль PlayStation 4 Slim',
                //         price: '44 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/2e00de8b4786143bcdfb6f8a5edbcc62/23ef531b89e6e0608e5ad56c97bf6fef5ef5f497ee9f4c6276e995ef2d00c494.jpg.webp',
                //     },
                //     {
                //         id: 14,
                //         title: 'Игровая консоль PlayStation 5 Digital Edition',
                //         price: '49 299 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/976d9d4a3edb4dd5b74ef33477d52508/12135f5e78851059c0aa25212425cbee8437d03a9dcb71a3ed31c64920b750ce.jpg.webp',
                //     },
                //     {
                //         id: 15,
                //         title: 'Сочинения в прозе. Александр Пушкин',
                //         price: '8 778 р.',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/27/226/2722620.jpg',
                //     },
                //     {
                //         id: 16,
                //         title: 'Yamaha MONTAGE6t',
                //         price: '444 000 р.',
                //         img: 'https://www.muztorg.ru/files/biw/5f8/bhf/koc/ook/wwk/s4k/s8c/o/biw5f8bhfkocookwwks4ks8co.jpg',
                //     },
                //     {
                //         id: 17,
                //         title: 'FOCUSRITE Scarlett 18i20 3rd Gen',
                //         price: '72 400 р.',
                //         img: 'https://www.muztorg.ru/files/36z/b26/pwb/fi8/cgs/4cw/g4w/kso/o/36zb26pwbfi8cgs4cwg4wksoo.jpg',
                //     },
                //     {
                //         id: 18,
                //         title: 'История государства Российского.Юбилейное издание.2 кн.',
                //         discount: '2 922 ₽',
                //         price: '3 299 ₽',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/25/726/2572693.jpg',
                //     },
                //     {
                //         id: 19,
                //         title: 'Принтер струйный Canon PIXMA G1420 [цветная печать, A4, 4800x1200 dpi, ч/б - 9.1 стр/мин (А4), USB-B, СНПЧ]',
                //         price: '17 499 ₽',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/200/200/066e011bff305be3ecb2a0532adb44c1/5966091faeca3adb3bd7b0d460a58662d08c7ed30a0c57ea697fd20de2d0d5e9.jpg.webp',
                //     },
                //     {
                //         id: 20,
                //         title: 'Смартфон Apple iPhone 11 128 ГБ черный',
                //         price: '49 999 р.',
                //         discount: '39 990 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/9951aa6a99611e4df95c83529680ba0f/c73bba26affbf44a01db51117e576f246bfd88a6402b11546368887a7f8ad707.jpg.webp',
                //     },
                //     {
                //         id: 21,
                //         title: 'KEPMA D1C Natural Matt',
                //         price: '13 700 р.',
                //         img: 'https://www.muztorg.ru/files/62d/13q/ei8/o00/c08/s4g/ww8/wkw/62d13qei8o00c08s4gww8wkw0.jpg',
                //     },
                //     {
                //         id: 22,
                //         title: '65" (163 см) Телевизор LED Xiaomi Mi TV 4S 65 серебристый',
                //         price: '59 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/7377b6b9fcdd0e463d55bd619eb6ee42/b9b8b99f9430272de6288608c0323a5743e452bcdc485e0ad7bb436648fe7e14.jpg.webp',
                //     },
                //     {
                //         id: 23,
                //         title: 'Игровая консоль PlayStation 4 Slim',
                //         price: '44 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/2e00de8b4786143bcdfb6f8a5edbcc62/23ef531b89e6e0608e5ad56c97bf6fef5ef5f497ee9f4c6276e995ef2d00c494.jpg.webp',
                //     },
                //     {
                //         id: 24,
                //         title: 'Игровая консоль PlayStation 5 Digital Edition',
                //         price: '49 299 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/976d9d4a3edb4dd5b74ef33477d52508/12135f5e78851059c0aa25212425cbee8437d03a9dcb71a3ed31c64920b750ce.jpg.webp',
                //     },
                //     {
                //         id: 25,
                //         title: 'Сочинения в прозе. Александр Пушкин',
                //         price: '8 778 р.',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/27/226/2722620.jpg',
                //     },
                //     {
                //         id: 26,
                //         title: 'Yamaha MONTAGE6t',
                //         price: '444 000 р.',
                //         img: 'https://www.muztorg.ru/files/biw/5f8/bhf/koc/ook/wwk/s4k/s8c/o/biw5f8bhfkocookwwks4ks8co.jpg',
                //     },
                //     {
                //         id: 27,
                //         title: 'FOCUSRITE Scarlett 18i20 3rd Gen',
                //         price: '72 400 р.',
                //         img: 'https://www.muztorg.ru/files/36z/b26/pwb/fi8/cgs/4cw/g4w/kso/o/36zb26pwbfi8cgs4cwg4wksoo.jpg',
                //     },
                //     {
                //         id: 28,
                //         title: 'История государства Российского.Юбилейное издание.2 кн.',
                //         discount: '2 922 ₽',
                //         price: '3 299 ₽',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/25/726/2572693.jpg',
                //     },
                //     {
                //         id: 29,
                //         title: 'Принтер струйный Canon PIXMA G1420 [цветная печать, A4, 4800x1200 dpi, ч/б - 9.1 стр/мин (А4), USB-B, СНПЧ]',
                //         price: '17 499 ₽',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/200/200/066e011bff305be3ecb2a0532adb44c1/5966091faeca3adb3bd7b0d460a58662d08c7ed30a0c57ea697fd20de2d0d5e9.jpg.webp',
                //     },
                //     {
                //         id: 30,
                //         title: 'Смартфон Apple iPhone 11 128 ГБ черный',
                //         price: '49 999 р.',
                //         discount: '39 990 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/9951aa6a99611e4df95c83529680ba0f/c73bba26affbf44a01db51117e576f246bfd88a6402b11546368887a7f8ad707.jpg.webp',
                //     },
                //     {
                //         id: 31,
                //         title: 'KEPMA D1C Natural Matt',
                //         price: '13 700 р.',
                //         img: 'https://www.muztorg.ru/files/62d/13q/ei8/o00/c08/s4g/ww8/wkw/62d13qei8o00c08s4gww8wkw0.jpg',
                //     },
                //     {
                //         id: 32,
                //         title: '65" (163 см) Телевизор LED Xiaomi Mi TV 4S 65 серебристый',
                //         price: '59 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/500/500/7377b6b9fcdd0e463d55bd619eb6ee42/b9b8b99f9430272de6288608c0323a5743e452bcdc485e0ad7bb436648fe7e14.jpg.webp',
                //     },
                //     {
                //         id: 33,
                //         title: 'Игровая консоль PlayStation 4 Slim',
                //         price: '44 999 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/2e00de8b4786143bcdfb6f8a5edbcc62/23ef531b89e6e0608e5ad56c97bf6fef5ef5f497ee9f4c6276e995ef2d00c494.jpg.webp',
                //     },
                //     {
                //         id: 34,
                //         title: 'Игровая консоль PlayStation 5 Digital Edition',
                //         price: '49 299 р.',
                //         img: 'https://c.dns-shop.ru/thumb/st1/fit/500/500/976d9d4a3edb4dd5b74ef33477d52508/12135f5e78851059c0aa25212425cbee8437d03a9dcb71a3ed31c64920b750ce.jpg.webp',
                //     },
                //     {
                //         id: 35,
                //         title: 'Сочинения в прозе. Александр Пушкин',
                //         price: '8 778 р.',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/27/226/2722620.jpg',
                //     },
                //     {
                //         id: 36,
                //         title: 'Yamaha MONTAGE6t',
                //         price: '444 000 р.',
                //         img: 'https://www.muztorg.ru/files/biw/5f8/bhf/koc/ook/wwk/s4k/s8c/o/biw5f8bhfkocookwwks4ks8co.jpg',
                //     },
                //     {
                //         id: 37,
                //         title: 'FOCUSRITE Scarlett 18i20 3rd Gen',
                //         price: '72 400 р.',
                //         img: 'https://www.muztorg.ru/files/36z/b26/pwb/fi8/cgs/4cw/g4w/kso/o/36zb26pwbfi8cgs4cwg4wksoo.jpg',
                //     },
                //     {
                //         id: 38,
                //         title: 'История государства Российского.Юбилейное издание.2 кн.',
                //         discount: '2 922 ₽',
                //         price: '3 299 ₽',
                //         img: 'https://cdn.img-gorod.ru/310x500/nomenclature/25/726/2572693.jpg',
                //     },
                //     {
                //         id: 39,
                //         title: 'Принтер струйный Canon PIXMA G1420 [цветная печать, A4, 4800x1200 dpi, ч/б - 9.1 стр/мин (А4), USB-B, СНПЧ]',
                //         price: '17 499 ₽',
                //         img: 'https://c.dns-shop.ru/thumb/st4/fit/200/200/066e011bff305be3ecb2a0532adb44c1/5966091faeca3adb3bd7b0d460a58662d08c7ed30a0c57ea697fd20de2d0d5e9.jpg.webp',
                //     },
                // ],
            }
        },
        components: {
            storeCatalogItem,
            storeSidebar,
        },
    };
</script>

<style>

.main {
    margin-top: 66px;
    flex: 1 1 auto;
}

.main__wrapper {
    width: 1170px;
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
}

.main__products {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
    width: 934px;
}

.pagination {
    width: 100%;
    height: 50px;
    border: 1px solid black;
    margin-bottom: 10px;
}

</style>