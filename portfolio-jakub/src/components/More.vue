<template>
    <div class="more">
        <div class="container">
            <div class="swedish">
                <h1>Swidish:</h1>
                <p>Fluently</p>
            </div>
            <div class="english">
                <h1>Endlish:</h1>
                <p>Fluently</p>
            </div>
            <div class="russian">
                <h1>Russian:</h1>
                <p>Basic</p>
            </div>
            <div class="polish">
                <h1>Polish:</h1>
                <p>Native language</p>
            </div>
            <div class="informations">
                <div class="information"> 
                    <h5>Character traits:</h5>
                    <p>Responsible, learns easily, enjoys learning from others, like to do things to the point where I'm proud of my work.</p>
                </div>
                <div class="information"> 
                    <h5>Interests:</h5>
                    <p>Playing instruments, skiing, fauna, psychology, electricity. It's really easier to list things I'm not interested in.</p>
                </div>
                <div class="information"> 
                    <h5>Citizenship:</h5>
                    <p>Swedish and Polish.</p>
                </div>
            </div>
            <div class="title">
                <h1>more.</h1>
            </div>
        </div>
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

@mixin style-item($border, $bg, $color) {
    border: 5px solid $border;
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    color: $color;
    background-color: $bg;
    font-size: 25px;

    h1 {
        margin: 0;
        font-weight: 300;
    }

    p {
        margin: 0;
        font-weight: 200;
    }
}

.more {
    width: 100%;
    display: flex;
    justify-content: center;
    margin: 50px 0px 50px 0px;

    .container {
        max-width: 1600px;
        display: grid;
        grid-template-rows: repeat(4, 400px);
        grid-template-columns: repeat(4, 400px);
        column-gap: 10px;
        row-gap: 10px;


        .swedish {
            @include style-item($yellow, #FFF, #000)
        }

        .english {
            grid-column-start: 2;
            grid-column-end: 4;
            @include style-item($yellow, #FFF, #000)
        }

        .russian {
            @include style-item($yellow, #FFF, #000)
        }

        .polish {
            grid-column-start: 1;
            grid-column-end: 3;
            @include style-item($yellow, #FFF, #000)
        }

        .informations {
            grid-column-start: 3;
            grid-column-end: 5;
            grid-row-start: 2;
            grid-row-end: 5;

            .information {
                width: 80%;
                margin: 25px 0px 25px 0px;
                
                h5 {
                    font-weight: 600;
                    font-size: 28px;
                    margin: 0;
                }

                p {
                    margin: 5px 0px 0px 10px;
                    font-weight: 100;
                    font-size: 20px
                }
            }

            @include style-item(#000, #000, #FFF);
        }

        .title {
            grid-column-start: 1;
            grid-column-end: 3;
            grid-row-start: 3;
            grid-row-end: 5;
            @include style-item(#000, #FFF, #000);

            border: 15px solid #000;

            h1 {
                font-weight: 700;
                font-size: 80px;
            }
        }
    }
}

@media only screen and (max-width: 1650px) {
    .more {
        .container {
            grid-template-rows: repeat(4, 350px);
            grid-template-columns: repeat(4, 350px);
        }
    }
}

@media only screen and (max-width: 1450px) {
    .more {
        .container {
            grid-template-rows: repeat(4, 250px);
            grid-template-columns: repeat(4, 250px);
        }
    }
}

@media only screen and (max-width: 1050px) {
    .more {
        .container {
            grid-template-rows: repeat(4, 200px);
            grid-template-columns: repeat(4, 200px);

            .swedish {
                font-size: 20px;
            }

            .english {
                font-size: 20px;
            }

            .russian {
                font-size: 20px;
            }

            .polish {
                font-size: 20px;
            }

            .informations {
                .information {
                    
                    h5 {
                        font-size: 23px;
                    }

                    p {
                        font-size: 15px
                    }
                }
            }

            .title {
                h1 {
                    font-weight: 700;
                    font-size: 60px;
                }
            }
        }
    }
}

@media only screen and (max-width: 850px) {
    .more {
        .container {
            grid-template-rows: repeat(4, 150px);
            grid-template-columns: repeat(4, 150px);

            .swedish {
                font-size: 15px;
            }

            .english {
                font-size: 15px;
            }

            .russian {
                font-size: 15px;
            }

            .polish {
                font-size: 15px;
            }

            .informations {
                .information {
                    margin: 10px 0px 10px 0px;
                    
                    h5 {
                        font-size: 23px;
                    }

                    p {
                        font-size: 15px
                    }
                }
            }

            .title {
                h1 {
                    font-weight: 700;
                    font-size: 60px;
                }
            }
        }
    }
}

@media only screen and (max-width: 650px) {
    .more {
        .container {
            grid-template-rows: repeat(4, 90px);
            grid-template-columns: repeat(4, 90px);

            .swedish {
                font-size: 10px;
            }

            .english {
                font-size: 10px;
            }

            .russian {
                font-size: 10px;
            }

            .polish {
                font-size: 10px;
            }

            .informations {
                .information {
                    margin: 10px 0px 10px 0px;
                    
                    h5 {
                        font-size: 10px;
                    }

                    p {
                        font-size: 10px
                    }
                }
            }

            .title {
                border: 10px solid #000;

                h1 {
                    font-weight: 700;
                    font-size: 40px;
                }
            }
        }
    }
}

@media only screen and (max-width: 420px) {
    .more {
        .container {
            grid-template-rows: repeat(4, 70px);
            grid-template-columns: repeat(4, 70px);

            .swedish {
                font-size: 8px;
            }

            .english {
                font-size: 8px;
            }

            .russian {
                font-size: 8px;
            }

            .polish {
                font-size: 8px;
            }

            .informations {
                .information {
                    margin: 5px 0px 5px 0px;
                    
                    h5 {
                        font-size: 10px;
                    }

                    p {
                        margin: 3px;
                        font-size: 8px
                    }
                }
            }

            .title {
                border: 8px solid #000;

                h1 {
                    font-weight: 700;
                    font-size: 40px;
                }
            }
        }
    }
}

</style>