<template>
    <div class="documents">

        <h1>documents.</h1>
        <div class="file">
            <a href="https://drive.google.com/file/d/1D8yDJF7RvdIwpzirqI7D5fYQJjEKiEQv/view?usp=share_link">
                <img src="../assets/img/cv.png" alt="cv">
                <h5>cv</h5>
            </a>
            <a href="https://drive.google.com/file/d/1hfVhXxF5AJb1NOoO4DnWy7bT8kUW188F/view?usp=share_link">
                <img src="../assets/img/reference.png" alt="reference">
                <h5>reference</h5>
            </a>
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

.documents {
    width: 100%;
    text-align: center;

    h1 {
        font-size: 80px;
    }

    .file {
        display: flex;
        align-items: center;
        

        a {
            text-decoration: none;
            padding: 50px;
            color: #000;
            cursor: pointer;
            width: 50%;

            img {
                width: 60%;
                border: 0.5px solid $yellow;
            }

            img:hover {
                box-shadow: 0px 0px 5px $yellow;
            }

            h5 {
                font-size: 50px;
                margin: 0px;
                font-weight: 300;
            }
        }
    }

}

@media only screen and (max-width: 1050px) {
    .documents {
        .file {
            display: flex;
            align-items: center;

            a {
                text-decoration: none;
                padding: 25px;
                color: #000;
                cursor: pointer;

                img {
                    width: 80%;
                }

                h5 {
                    font-size: 40px;
                }
            }
        }
    }
}

@media only screen and (max-width: 550px) {
    .documents {

        h1 {
            font-size: 50px;
        }

        .file {
            display: flex;
            align-items: center;

            a {
                text-decoration: none;
                padding: 25px;
                color: #000;
                cursor: pointer;

                img {
                    width: 80%;
                }

                h5 {
                    font-size: 25px;
                }
            }
        }
    }
}

</style>