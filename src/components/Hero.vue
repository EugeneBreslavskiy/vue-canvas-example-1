<template>
    <div class="hero">
        <h2 class="hero__title">
            Move cursor for interaction
        </h2>
        <video class="hero__video" autoplay="true" loop="true" muted="true">
            <source src="../assets/videos/video.mp4" type="video/mp4">
        </video>
        <canvas class="hero__canvas" ref="canvas" @mousemove="draw"></canvas>
    </div>
</template>

<script>
export default {
    name: 'Hero',
    data() {
        return {
            ctx: null
        }
    },
    methods: {
        initCanvas() {
            let canvas = this.$refs.canvas;
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;

            this.ctx = canvas.getContext('2d');

            this.ctx.fillStyle = '#FFFFFF';
            this.ctx.fillRect(0, 0, canvas.width, canvas.height);
            this.ctx.globalCompositeOperation = 'destination-out';
        },
        draw(e) {
            this.ctx.beginPath();
            this.ctx.arc(e.clientX, e.clientY, 50, 0, Math.PI * 2);
            this.ctx.fill();
        }
    },
    mounted() {
        this.initCanvas();
    }
}
</script>

<style lang="scss">
.hero {
    min-height: 100vh;
    position: relative;
}
.hero__title {
    width: 600px;
    margin: 0;
    font-size: 60px;
    font-weight: 900;
    text-align: right;
    position: absolute;
    right: 50px;
    bottom: 50px;
    z-index: 10;
    pointer-events: none;
}
.hero__video {
    min-width: 100%;
    min-height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
}
.hero__canvas {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 5;
}
</style>