<template>

    <div class="box" :style="{ transform: 'skewY(-' + angle + 'deg)' }">
    </div>
    
    
</template>

<script>
export default {
    data() {
        return {
            angle: 0
        }
    },
    created() {
        this.calculateTransform();
        window.addEventListener('resize', this.calculateTransform);
    },
    beforeDestroy() {
        window.removeEventListener('resize', this.calculateTransform);
    },

    methods: {
        calculateTransform() {
            var angle = Math.atan(window.innerHeight / window.innerWidth) * (180 / Math.PI);
            this.angle = angle;
        }
    }
}

</script>

<style lang="scss" scoped>
.box {
    margin-top: 50vh;
    position: fixed;
    top: 0; // this is particular element, if erase it FIXED will break
    height: 200vw;
    width: 100vw;
    background-image: url('/src/assets/flow1.gif');
    background-repeat: no-repeat;
    background-size: cover;
    background-color: cadetblue;
    opacity: 0.8;
    background-size: 100% 60%;
    z-index: -2;
    filter: blur(3px);
}

</style>