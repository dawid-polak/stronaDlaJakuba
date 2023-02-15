<template>
    <div class="button">
        <div class="box box-color"></div>
        <div class="box box-border"></div>
        Read more
    </div>
</template>

<script>
export default {
    setup () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>

@import '../style/style.scss';

.button {
    width: 200px;
    height: 60px;
    color: #FFF;
    display: flex;
    font-size: 20px;
    font-weight: 600;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    position: relative;

    .box {
        position: absolute;
        width: 200px;
        height: 60px;
    }

    .box-color {
        background-color: $yellow;
        z-index: -100;
    }

    .box-border {
        border: 1.5px solid #000;
        top: -6px;
        left: 6px;
        animation: btnBack 0.25s ease-in-out forwards;
    }

    .box-border:hover {
        animation: btn 0.25s forwards;
    }

}

@keyframes btnBack {
    0% {
            top: 6px;
            left: -6px;
    }
    100% {
            top: -6px;
            left: 6px;
    }
}

@keyframes btn {
    0% {
        top: -6px;
        left: 6px;
    }
    100% {
        top: 6px;
        left: -6px;
    }
}
</style>