<template>
    <div class="grid">
        <div class="row1 row">
            <div class="cell"></div>
            <div class="cell"></div>
            <div class="cell"></div>
            <div class="cell"></div>
        </div>
        <div class="row2 row">
            <div class="cell"></div>
            <div class="cell"></div>
            <div class="cell"></div>
        </div>
        <div class="row3 row">
            <div class="cell"></div>
            <div class="cell"></div>
            <div class="cell"></div>
            <div class="cell"></div>
        </div>
    </div>
</template>

<script>
import bigCircleL from '/src/bigCircleLeft.vue';
import bigCircleR from '/src/bigCircleRight.vue';

export default {
    components: {
        bigCircleL,
        bigCircleR
    }
}
</script>
<style lang="scss" scoped>
@import './variables';

.grid {
    display: grid;
    grid-template-rows: 1fr 2fr 1fr;
}

.row {
    display: grid;
}

.row1 {
    grid-template-columns: 3fr 1fr 4fr 3fr;
}

.row2 {
    grid-template-columns: 5fr 2fr 5fr;
}

.row3 {
    grid-template-columns: 1fr 3fr 4fr 2fr;
}

.cell {
    display: flex;
    align-items: center;
    justify-content: center;
}

@if $debug {
    
    .cell {
        opacity: 0.5;
        border: 1px solid #333;
    }

    .cell>* {
        opacity: 1;
    }

    .row .cell:nth-child(1) {
        background-color: #ff9999;
    }

    .row .cell:nth-child(2) {
        background-color: #99ff99;
    }

    .row .cell:nth-child(3) {
        background-color: #9999ff;
    }

    .row .cell:nth-child(4) {
        background-color: #ffff99;
    }
}
</style>