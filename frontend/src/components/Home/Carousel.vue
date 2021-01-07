<template>
    <el-carousel id="carrouselSection" trigger="click" arrow="never" height="100vh">
            <el-carousel-item v-for="item in itens" :key="item.id">
                <el-row class="darken-filter" :style="{ backgroundImage: `url(${item.photo})` }">
                    <el-col align="center" class="carousel-item-content">
                        <h2>{{ item.title }}</h2>
                        <p>{{ item.description }}</p>
                        <ContactButton/>
                    </el-col>
                </el-row>
            </el-carousel-item>
    </el-carousel>
</template>

<style lang="scss">
    @import '../../styles/variables.scss';

    .el-carousel__item{
        
            .el-row {
                background-repeat: no-repeat;
                background-size: cover;
            }            
        }

        .el-carousel__indicators {
            bottom: 4% !important;

            .is-active {

                .el-carousel__button {
                    background-color: white !important;
                }
            }

            .el-carousel__button {
                height: 4px !important;
            }
        }

        .carousel-item-content {
            display: flex;
            justify-content: center;
            flex-direction: column;
            align-items: center;
            z-index: 2 !important;
            height: 100vh;
            h2 {
                font-size: 6em;
                color: #FEFEFE;
                font-weight: 100;
                margin: 0;
                width: 90%;

                b {
                    font-weight: 700;
                }
            }

            p {
                font-size: 30px;
                width: 50%;
                font-weight: 300;
                color: #FEFEFE;
            }

        }

        @media only screen and (max-width: 1024px) {
            .carousel-item-content {

                p {
                    width: 80%;
                }
            }
        }

        @media only screen and (max-width: 600px) {
            .carousel-item-content {

                h2 {
                    width: 93%;
                    font-size: 2em;
                }

                p {
                    font-size: 1.5em;
                }
            }
        }
  
</style>

<script>
import ContactButton from "../ContactButton"

export default {
    data() {
        return {
            itens: [
                {
                    id: 0,
                    title: "Exclusivade ",
                    description: "Inspiramos você a pensar grande!",
                    photo: require("../../assets/background1.png")
                },
                {
                    id: 1,
                    title: "Qualidade",
                    description: "Nossa satisfação é você!",
                    photo: require("../../assets/background2.png")
                },
                {
                    id: 2,
                    title: "Requinte",
                    description: "Buscamos constatemente a transformação, evolução e modernização!",
                    photo: require("../../assets/background3.png")
                },
            ],
        }
    },

    components: {
        ContactButton,
    },
}
</script>