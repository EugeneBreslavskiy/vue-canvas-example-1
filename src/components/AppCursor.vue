<template>
    <div class="cursor" ref="cursor"></div>
</template>

<script>
export default {
    name: 'app-cursor',
    methods: {
        initCursor() {
            document.addEventListener('mousemove', (e) => {
                const { clientX, clientY } = e;
                this.$refs.cursor.style.left = `${ clientX - 20 }px`;
                this.$refs.cursor.style.top = `${ clientY - 20 }px`;
            });
        }
    },
    mounted() {
        this.initCursor();
    }
}
</script>

<style lang="scss">
.cursor {
    width: 40px;
    height: 40px;
    box-sizing: border-box;
    border: 4px solid #1f3649;
    border-radius: 50%;
    position: absolute;
    z-index: 15;
    pointer-events: none;
}
</style>