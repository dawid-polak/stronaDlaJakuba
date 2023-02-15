<template>
    <div class="footer">
        <div class="left">
            <h1>contact me.</h1>
        </div>
        <div class="right">
            <h1>contact me.</h1>
            <div class="box"> 
                <img src="../assets/icons/email.png" alt="email"> 
                <a href="mailto: kubajarecki1205@gmail.com">kubajarecki1205@gmail.com</a>
            </div>
            <div class="box">
                <img src="../assets/icons/telephone.png" alt="phone">
                <a href="tel:+46 722 58 38 99">+46 722 58 38 99 </a>
                <a href="tel:+48 606 341 688"> +48 606 341 688</a>
            </div>
            <div class="box">
                <img src="../assets/icons/home.png" alt="home">
                Forvägen 1, lgh 1002 145 51 <br> Norsborg Stockholm, Sweden
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

.footer {
    width: 100%;
    min-height: 500px;
    background-color: #000;
    color: #FFF;
    display: flex;
    align-items: center;
    .left {
        width: 50%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: end;

        h1 {
            font-size: 80px;
            margin-bottom: 60px;
        }
    }

    .right {
        width: 50%;
        height: 100%;
        color: #FFF;
        display: flex;
        flex-flow: column;
        justify-content: center;

        h1 {
            display: none;
        }
        .box {
            height: 70px;
            display: flex;
            align-items: center;
            font-size: 35px;
            font-weight: 200;
            margin: 25px;

            img { 
                width: 70px;
                margin: 40px;
            }

            a {
                text-decoration: none;
                color: #FFF;
                margin-right: 20px;
            }

            a:hover {
                color: $yellow;
            }
        }
    }
}

@media only screen and (max-width: 1530px) {
    .footer {
        .left {
            h1 {

            }
        }

        .right {
            .box {
                font-size: 30px;

                img { 
                    width: 70px;
                    margin: 40px;
                }

                a {
                    text-decoration: none;
                    color: #FFF;
                    margin-right: 20px;
                }
            }
        }
    }
}

@media only screen and (max-width: 1380px) {
    .footer {
        .left {
            h1 {

            }
        }

        .right {
            .box {
                font-size: 25px;

                img { 
                    width: 70px;
                    margin: 40px;
                }

                a {
                    text-decoration: none;
                    color: #FFF;
                    margin-right: 20px;
                }
            }
        }
    }
}

@media only screen and (max-width: 1230px) {
    .footer {
        .left {
            h1 {
                font-size: 70px;
            }
        }

        .right {
            .box {
                font-size: 18px;
                margin: 15px;
                height: 60px;

                img { 
                    width: 50px;
                    margin: 30px;
                }

                a {
                    text-decoration: none;
                    color: #FFF;
                    margin-right: 10px;
                }
            }
        }
    }
}

@media only screen and (max-width: 970px) {
    .footer {
        .left {
            h1 {
                font-size: 45px;
            }
        }

        .right {
            .box {
                font-size: 16px;
                margin: 10px;
                height: 50px;

                img { 
                    width: 40px;
                    margin: 20px;
                }

                a {
                    text-decoration: none;
                    color: #FFF;
                    margin-right: 10px;
                }
            }
        }
    }
}

@media only screen and (max-width: 730px) {
    .footer {
        .left {
            display: none;
        }

        .right {
            width: 100%;

            h1 {
                display: block;
                font-size: 40px;
                text-align: center;
                margin-top: 0;
            }
            .box {
                font-size: 16px;
                margin: 10px;
                height: 50px;

                img { 
                    width: 40px;
                    margin: 20px;
                }

                a {
                    text-decoration: none;
                    color: #FFF;
                    margin-right: 10px;
                }
            }
        }
    }
}

</style>