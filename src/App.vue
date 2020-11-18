<template>
    <div id="app">
        <Hero/>
    </div>
</template>

<script>
import Hero from './components/Hero.vue'

export default {
    name: 'App',
    components: {
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
