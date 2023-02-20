<template>
    <div class="skills">
        <img class="img" src="../assets/img/about.jpeg" alt="about">
        <h1>skills.</h1>
        <div class="container">
            <div v-for="skill in dataRef" :key="skill" class="skill">
                <p>{{ skill.name }}</p>
                <input class="skill-input" type="range" min="1" max="100" :value="0" style="">
                <p>{{ skill.percent }}%</p>
            </div>
        </div>
    </div>
</template>

<script>
import { onMounted, onUnmounted, onUpdated, ref } from 'vue';
import data from '../assets/data/skills.json';

export default {
    setup () {
        const dataRef = ref();
        dataRef.value = data.skills;
        
        onMounted(() => {
            
            const inputsSkill = document.querySelectorAll('.skill-input');
            const percent = ref([])

            dataRef.value.forEach((skill) => {
                percent.value.push(skill.percent)
            })
            
            inputsSkill.forEach((input, x) => {
                //if you want add new skill with another value you have to add class in css
                const classValue = ref(`input-white-${percent.value[x]}`);

                input.classList.add(`${classValue.value}`)
            })
        })
        

        return { dataRef }
    }
}
</script>

<style lang="scss" scoped>

@import '../style/style.scss';

.skills {
    width: 100%;
    background-color: $yellow;

    h1 {
        font-size: 80px;
        text-align: center;
        color: #FFF;
        padding: 30px;
        margin: 0;
    }


    .container {
        padding-bottom: 50px;
        margin: 0 auto 0 auto;
        width: 80%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-flow: column;
        
        .skill {
            width: 80%;
            text-align: center;
            margin: 15px;

            p {
            text-align: left;
            width: 80%;
            margin: 4px;
            font-size: 20px;
            color: #FFF;
            font-weight: 400;
            }

            input {
                border: 0;
                width: 100%;
                background: #000;
                border-radius: 10px;
                overflow: hidden;
                appearance: none;
            }

            //chrome
            input::-webkit-slider-thumb {
                -webkit-appearance: none;
                appearance: none;
                width: 15px;
                height: 15px;
                background-color: #FFF;
                width: 100%;
            }

            .input-white-60::-webkit-slider-thumb {
                margin-left: -40%;
            }
            .input-white-80::-webkit-slider-thumb {
                margin-left: -20%;
            }

            .input-white-85::-webkit-slider-thumb {
                margin-left: -15%;
            }

            .input-white-90::-webkit-slider-thumb {
                margin-left: -10%;
            }
            .input-white-95::-webkit-slider-thumb {
                margin-left: -5%;
            }
            .input-white-100::-webkit-slider-thumb {
                margin-left: 0%;
            }

            //mozzila
            input::-moz-range-thumb {
                height: 18px;
                background-color: #FFF;
                border: 0;
                left: 0;
            }
            .input-white-60::-moz-range-thumb {
                width: 60%;
            }
            .input-white-80::-moz-range-thumb {
                width: 80%;
            }

            .input-white-85::-moz-range-thumb {
                width: 85%;
            }

            .input-white-90::-moz-range-thumb {
                width: 90%;
            }
            .input-white-95::-moz-range-thumb {
                width: 95%;
            }
            .input-white-100::-moz-range-thumb {
                width: 100%;
            }
        }
    }

    img {
        display: none;
    }
}

@media only screen and (max-width: 650px) {
    .skills {
        h1 {
            margin-top: -120px;
            font-size: 60px;
        }

        .container {
            padding-bottom: 50px;
            width: 95%;
            
            .skill {
                width: 90%;
                margin: 5px;

                p {
                text-align: left;
                width: 80%;
                margin: 4px;
                font-size: 20px;
                color: #FFF;
                font-weight: 400;
                }

                input {
                    border: 0;
                    width: 100%;
                    background: #000;
                    border-radius: 10px;
                    overflow: hidden;
                    appearance: none;
                }

                input::-webkit-slider-thumb {
                    -webkit-appearance: none;
                    appearance: none;
                    width: 8px;
                    height: 8px;
                    background-color: #FFF;
                    width: 100%;
                }
            }
        }

        .img {
            display: block;
            width: 100%;
        }
    }
}

</style>