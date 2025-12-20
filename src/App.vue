<template>
  <div id="app">
    <header-component />
    <router-view />
  </div>
</template>

<script lang="js" >
import Header from './components/primari/Header.vue';
export default {
  name: 'App',
  data() {
    return {
      message: ' !'
    }
  }
}
</script>

<style lang="scss">
@import "/src/assets/css/index.css";
@import "/src/assets/sass/index.scss";
// Здесь ваши глобальные стили (пока пустые)
</style>
