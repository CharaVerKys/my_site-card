<template>
    <div class="grid">
        <div class="row1 row">
            <div class="cell">swcmdins links</div> 
            <div class="cell"></div>
            <div class="cell">dynemic</div>
            <div class="cell">extra links</div>
        </div>
        <div class="row2 row">
            <div class="cell">leftCircle and neuro</div>
            <div class="cell"><linuxlogo></linuxlogo></div>
            <div class="cell">rightCircle</div>
        </div>
        <div class="row3 row">
            <div class="cell"></div>
            <div class="cell"></div>
            <div class="cell">car</div>
            <div class="cell"></div>
        </div>
    </div>
</template>

<script>
import linuxlogo from './gridCells/linux.vue';


export default {
    components: {   
        linuxlogo
    }
}
</script>
<style lang="scss" scoped>
@import './variables';

.grid {
    position: relative;
    z-index: 1;
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
        border: 1px solid #33333380;
    }

    .row .cell:nth-child(1) {
        background-color: #ff999980;
    }

    .row .cell:nth-child(2) {
        background-color: #99ff9980;
    }

    .row .cell:nth-child(3) {
        background-color: #9999ff80;
    }

    .row .cell:nth-child(4) {
        background-color: #ffff9980;
    }
}
</style>