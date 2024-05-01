<template>
    <div class="box" :style="{ transform: 'skewY(' + angle + 'deg)' }">
        <div class="textLayer" :style="{ transform: 'skewY(-' + angle + 'deg)' }">
            <p class="pc">Chara_VerKys</p>
            <p class="pc">Junior c++ and</p>
            <p class="pc">web-fullstack developer</p>
            <br>
            <p class="flexerP"> <a class="bottomText extraString" href="https://discord.com/users/573917915368390676/">discordID</a>
                <a class="bottomText mainstr" href="https://t.me/Chara_VerKys">@Chara_VerKys</a>
                <span class="bottomText extraString" >charaverk@gm.c</span>
            </p>
        </div>
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


<style lang="scss" scoped>
.box {
    margin-top: 50vh;
    position: fixed;
    top: 0; // this is particular element, if erase it FIXED will break
    height: 200vw;
    width: 100vw;
    z-index: 2;
    display: flex;
    flex-direction: row;
    right: 25vw;
    top: 25vh;
    opacity: 0.8;

    .textLayer {
        font-size: 1.2em;
        position: absolute;
        text-align: center;
        z-index: 10;
        pointer-events: none;
        margin-top: 10vh;
        margin-right: 23vw;

        .pc {
            transform: rotate(-7deg);
            transform-origin: center;
            pointer-events: all;
            height: fit-content;
            width: fit-content;
            margin: 0 auto;
        }

        .bottomText {
            opacity: 0.9;
            pointer-events: all;
            color: black;
        }
        .mainstr{
            margin: 0 2vw;
        }
        @media screen and (max-width: 1200px) {
            .extraString{
                display: none;
            }
        }

    }


    #left {
        filter: blur(2px);
        flex: 1;

        #backgroundLeft {
            background-image: url('/src/assets/pattern_for_link.png');
            margin-top: 50vh;
        }
    }

    #backgroundRight {
        filter: blur(2px);
        flex: 1;
        background-image: url('/src/assets/pattern_for_link.png');
    }

}
</style>