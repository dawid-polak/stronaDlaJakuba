<template>
    <div class="about">
        <div class="border">
            <div class="box-left">
                <img src="../assets/img/about.jpeg" alt="about">
                <h1>about.</h1>
            </div>
            <div class="box-right">
                <div>
                    <div class="m-title">about.</div>
                    <p>{{ text.pargFirst }}</p>
                    <p>{{ text.pargSecound }}</p>
                    <p>{{ text.pargThird }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue'
import data from '../assets/data/about.json'

export default {
    setup () {
        const text = ref();
        text.value = data;

        return { text }
    }
}
</script>

<style lang="scss" scoped>

@import '../style/style.scss';

.about {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    .border {
        width: 90%;
        border: 5px solid $yellow;
        display: flex;

        .box-left {
            width: 40%;
            display: flex;
            flex-flow: column;
            align-items: center;
            justify-content: space-between;

            img {
                margin-top: 15vh;
                width: 40%;
                
            }

            h1 {
                margin-top: 20%;
                font-size: 80px;
                color: $yellow;
            }

        }

        .box-right {
            width: 60%;
            display: flex;
            justify-content: center;
            align-items: center;

            div {
                margin: 10%;

                p {
                    font-size: 28px;
                    font-weight: 300;
                }
            }

            .m-title {
                display: none;
            }
        }
    }
}

@media only screen and (max-width: 1950px) {
    .about {
        .border {
            .box-left {

            }
            .box-right {
                div {
                    margin: 10%;

                    p {
                        font-size: 25px;
                        font-weight: 300;
                    }
                }
            }
        }
    }
}

@media only screen and (max-width: 1740px) {
    .about {
        .border {
            .box-left {

            }
            .box-right {
                div {
                    margin: 10%;

                    p {
                        font-size: 22px;
                        font-weight: 300;
                    }
                }
            }
        }
    }
}

@media only screen and (max-width: 1540px) {
    .about {
        .border {
            .box-right {
                div {
                    margin: 10%;

                    p {
                        font-size: 20px;
                        font-weight: 300;
                    }
                }
            }
        }
    }
}

@media only screen and (max-width: 1240px) {
    .about {
        .border {
            .box-left {

            }
            .box-right {
                div {
                    margin: 10%;

                    p {
                        font-size: 18px;
                        font-weight: 300;
                    }
                }
            }
        }
    }
}

@media only screen and (max-width: 750px) {
    .about {
        .border {
            .box-left {
                display: none;
            }
            .box-right {
                
                width: 100%;
                div {
                    margin: 10%;
                    z-index: 100;

                    p {
                        font-size: 16px;
                        text-align: justify;
                        font-weight: 300;
                    }
                }
                .m-title {
                    display: block;
                    font-size: 45px;
                    font-weight: 700;
                    color: $yellow;
                }
            }
        }
    }
}

</style>