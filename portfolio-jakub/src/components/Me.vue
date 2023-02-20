<template>
    <div class="me">
        <p>Created by</p>
        <a href="http://dawidpolak.pl" target="_blanc">Dawid Polak</a>
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

.me {
    width: 100%;
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content: center;
    font-size: 12px;
    margin: 5px 0px 5px 0px;

    p {
        margin: 0;
    }

    a {
        color: $yellow;
        font-weight: 500;
        cursor: pointer;
    }
}

</style>