<template>
    <div class="experiences">
        <img src="../assets/img/home.png" alt="home">
        <h1>experiences.</h1>
        <div class="container">

            <div v-for="e in refData" :key="e.id">
                <ItemExperience :data="e" />
            </div>
            
        </div>
    </div>
</template>

<script>
import { ref } from 'vue'
import ItemExperience from './ItemExperience.vue';
import data from '../assets/data/experience.json';

export default {
    components: {
        ItemExperience
    },
    setup () {
        const refData = ref(null);
        refData.value = data.experiences;

        return { refData }
    }
}
</script>

<style lang="scss" scoped>

@import '../style/style.scss';

.experiences {
    margin-bottom: 100px;
    margin-top: 100px;
    width: 100%;

    img {
        display: none;
    }

    h1 {
        text-align: center;
        font-size: 80px;
        margin-bottom: 80px;
    }

    .container {
        margin: auto;
        width: 90%;
    }
}

@media only screen and (max-width: 750px) {
    .experiences {


        img {
            display: block;
            width: 100%;
            margin-top: -250px;
        }

        h1 {
            font-size: 55px;
            margin-bottom: 40px;
        }

        .container {
        margin: auto;
        width: 85%;
    }
}
}

</style>