<template>
  <div id="app">
    <header-component />
    <router-view />
  </div>
</template>

<script>
import Header from './components/primari/Header.vue';

</script>

<style lang="scss">
@import "/src/assets/css/index.css";
@import "/src/assets/sass/index.scss";
// Здесь ваши глобальные стили (пока пустые)
</style>
