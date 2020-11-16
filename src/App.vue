<template>
    <div id="app">
        <AppCursor/>
        <Hero/>
    </div>
</template>

<script>
import AppCursor from './components/AppCursor.vue'
import Hero from './components/Hero.vue'

export default {
    name: 'App',
    components: {
        AppCursor,
        Hero
    }
}
</script>

<style lang="scss">
@font-face {
    font-family: 'Montserrat';
    src: url('./assets/fonts/Montserrat/Montserrat-Thin.ttf');
    src: local('Montserrat Thin'), local('Montserrat-Thin'),
    url('./assets/fonts/Montserrat/Montserrat-Thin.ttf') format('truetype');
    font-weight: 100;
    font-style: normal;
}

@font-face {
    font-family: 'Montserrat';
    src: url('./assets/fonts/Montserrat/Montserrat-Black.ttf');
    src: local('Montserrat Black'), local('Montserrat-Black'),
    url('./assets/fonts/Montserrat/Montserrat-Black.ttf') format('truetype');
    font-weight: 900;
    font-style: normal;
}

body {
    margin: 0;
    font: 16px 'Montserrat', sans-serif;
    cursor: none;
}
#app {
    position: relative;
    overflow: hidden;
}
</style>
