<template>
    <div class="logo">
        <a href="https://lx4u.ru/">
            <img src="../../assets/linuxlogo.png">
        </a>
    </div>
</template>
<style lang="scss" scoped>
.logo {
    display: flex;
    align-items: center;

    a {
        width: 150%;
        transform: rotate(7deg);

        height: fit-content;
    }

    img {
        width: 120%;
        height: auto;
        margin-left: -10%;
    }
}
</style>