<template>
  <div class="wrapper">
    <!-- шапка сайта -->
    <storeHeader/>

    <!-- каталог сайта -->
    <storeCatalog/>

    <upBtn style="user-select: none;"/>

    <!-- подвал сайта -->
    <storeFooter/>

  </div>
</template>

<script>
import storeHeader from './components/store-header.vue';
import storeCatalog from './components/store-catalog.vue';
import storeFooter from './components/store-footer.vue';
import upBtn from './components/up-btn.vue';

export default {
  name: 'App',
  components: {
    storeHeader,
    storeCatalog,
    storeFooter,
    upBtn
  }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style: none;
}

html, body {
  height: 100%;
}

.wrapper {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>