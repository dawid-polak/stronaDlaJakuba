<template>
    <div ref="navbar" class="navbar">
        <img src="../assets/img/logo.png" alt="logo">
    </div>  
</template>

<script>
import { onMounted, ref } from 'vue'

export default {

    setup () {
        const navbar = ref(null);
        onMounted(() => {
            window.addEventListener('scroll', () => {
                if ( window.scrollY > 30 ) {
                    navbar.value.classList.add('navbar-scroll')
                } else {
                    navbar.value.classList.remove('navbar-scroll')
                }
            })
        
        })

        return { navbar }
    }
}
</script>

<style lang="scss" scoped>

@use '../style/style.scss';
.navbar {
    z-index: 1000;
    background-color: #FFF;
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    top: 0;
    animation: removescroll 0.5s forwards;

    img {
        height: 70px;
    }
}

.navbar-scroll {
    animation: addscroll 0.5s forwards;
}

@keyframes addscroll {
    0% {
        box-shadow: 0;
    } 
    100% {
        box-shadow: 0 1px 10px -2px gray;
    }
}

@keyframes removescroll {
    0% {
        box-shadow: 0 1px 10px -2px gray;
    } 
    100% {
        box-shadow: 0;
    }
}

</style>