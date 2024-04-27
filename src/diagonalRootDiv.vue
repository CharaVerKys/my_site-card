<template>

    <div class="box box1" :style="{ transform: 'skewY(-' + angle + 'deg)' }">
    </div>
    <div class="box box2" :style="{ transform: 'skewY(' + angle + 'deg)' }">
        <div id="left" :style="{ transform: 'skewY(-' + angle + 'deg)' }">
            <div id="backgroundLeft" :style="{ transform: 'skewY(-' + angle + 'deg)' }"></div>
        </div>
        <div id="backgroundRight"></div>

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

<style lang="scss">
.box {
    margin-top: 50vh;
    position: fixed;
    top: 0; // this is particular element, if erase it FIXED will break
    height: 200vw;
    width: 100vw;
}

.box1 {
    background-image: url('/src/assets/flow1.gif');
    background-repeat: no-repeat;
    background-size: cover;
    background-size: 100% 60%;
    z-index: -2;
}


.box2 {
    z-index: -1;
    display: flex;
    flex-direction: row;
    right: 25vw;
    top: 25vh;

    #left {
        flex: 1;
        #backgroundLeft {
            background-color: green;
            margin-top: 50vh;
        }
    }

    #backgroundRight {
        flex: 1;
        background-color: red;
    }

}
</style>