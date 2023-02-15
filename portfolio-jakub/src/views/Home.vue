<template>
    <div>
        <Navbar />
        <div class="home">
            <div class="box box-left">
                <img src="../assets/img/home.png" alt="home">
            </div>
            <div class="box box-right">
                <div>
                    <span>Hi,</span> <br>
                    <span>I am an electrician</span> <br> <br>
                    <span>Jakub Matuszczak</span>
                </div>
                <div>
                    <hr>
                    <a @click="scrollToAbout"> <Btn /> </a>
                </div>
            </div>
        </div>
        <div ref="aboutTo">
            <About/>
        </div>
        <Experiences />
        <Skills />
        <More />
        <Education />
        <Documents />
        <Footer />
        <Me />
    </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
import Btn from '../components/Btn.vue'
import About from '../components/About.vue'
import Experiences from '../components/Experiences.vue';
import Footer from '../components/Footer.vue'
import More from '../components/More.vue'
import Skills from '../components/Skills.vue';
import Education from '../components/Education.vue';
import Documents from '../components/Documents.vue';
import Me from '../components/Me.vue'

import { ref } from 'vue';

export default {
    components: {
        Navbar,
        Btn,
        About,
        Experiences,
        Footer,
        More,
        Skills,
        Education,
        Documents,
        Me
    },
    setup () {
        const aboutTo = ref();
        
        const scrollToAbout = () => {

            aboutTo.value.scrollIntoView({behavior: "smooth"})

        }
 
        return {scrollToAbout, aboutTo }
    }
}
</script>

<style lang="scss" scoped>

@import '../style/style.scss';


//welcome-section
.home {
    height: calc(100vh - 80px);
    display: flex;

    .box {
        width: 50%;
        height: 100%;
        display: flex;
    }

    .box-left {
        display: flex;
        align-items: center;
        justify-content: center;

        img {
            width: 50%;
        }
    }

    .box-right {
        flex-flow: column;
        justify-content: center;
        
        span:first-child {
            color: $yellow;
            font-size: 120px;
            font-weight: 600;
        }

        span {
            margin-top: 10px;
            font-size: 50px;
            font-weight: 300;
        }
        
        span:last-child {
            font-size: 70px;
            font-weight: 700;
        }

        hr {
            width: 50%;
            margin: 20px 0px 20px 0px;
        }

        a {
            text-decoration: none;
        }
    }   
}


//breakponit 

@media only screen and (max-width: 1380px) {
    .home {
        .box-right {
            
            span:first-child {
                font-size: 100px;
            }

            span {
                margin-top: 10px;
                font-size: 45px;
            }
            
            span:last-child {
                font-size: 60px;
            }

            hr {
                width: 50%;
                margin: 20px 0px 20px 0px;
            }
        }   
    }
}

@media only screen and (max-width: 1080px) {
    .home {
        .box-right {
            
            span:first-child {
                font-size: 80px;
            }

            span {
                margin-top: 10px;
                font-size: 35px;
            }
            
            span:last-child {
                font-size: 50px;
            }

            hr {
                width: 50%;
                margin: 20px 0px 20px 0px;
            }
        }   
    }
}

@media only screen and (max-width: 880px) {
    .home {
        .box-left {
            display: none;
        }
        .box-right {
            width: 100%;
            margin-left: 20vw;
            
            span:first-child {
                font-size: 80px;
            }

            span {
                margin-top: 10px;
                font-size: 35px;
            }
            
            span:last-child {
                font-size: 50px;
            }

            hr {
                width: 50%;
                margin: 20px 0px 20px 0px;
            }
        }   
    }
}

@media only screen and (max-width: 580px) {
    .home {
        .box-left {
            display: none;
        }
        .box-right {
            width: 100%;
            margin-left: 20vw;
            
            span:first-child {
                font-size: 70px;
            }

            span {
                margin-top: 10px;
                font-size: 25px;
            }
            
            span:last-child {
                font-size: 35px;
            }

            hr {
                width: 50%;
                margin: 20px 0px 20px 0px;
            }
        }   
    }
}
</style>