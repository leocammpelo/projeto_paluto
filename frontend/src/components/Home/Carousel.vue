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
                    title: "Olá, sou o Leonardo Campelo",
                    description: "Sou Estudante!",
                    photo: "https://bn1303files.storage.live.com/y4m7Jqc2cei8lsPtx53bSwQSEgyO2dYA1pA56FPITgmSg9aZ2t8Ji0osa5MxN5NIuYNVGR6VXKEcYvNC4ETo_fERyndzgkk93DrYwmFteQH5tB01ZqMhUa-AAlJRc54GpuSRe5Hh9jHzFlv0fcXHJwxbHVufpPnlxQirvs9rZeMGVR2z3245Yt2YJHWBqvVM4dWSalUoVL7bP0PfLIrvjBOog/Cena%2007_Gebbwork_Escritorio%20Yaris_Carvalho%20Claro%20e%20Preto_Variacao%2003.jpg?psid=1&width=1292&height=862"
                },
                {
                    id: 1,
                    title: "Olá, sou o Leonardo Campelo",
                    description: "Sou Estudante!",
                    photo: "https://bn1303files.storage.live.com/y4m7Jqc2cei8lsPtx53bSwQSEgyO2dYA1pA56FPITgmSg9aZ2t8Ji0osa5MxN5NIuYNVGR6VXKEcYvNC4ETo_fERyndzgkk93DrYwmFteQH5tB01ZqMhUa-AAlJRc54GpuSRe5Hh9jHzFlv0fcXHJwxbHVufpPnlxQirvs9rZeMGVR2z3245Yt2YJHWBqvVM4dWSalUoVL7bP0PfLIrvjBOog/Cena%2007_Gebbwork_Escritorio%20Yaris_Carvalho%20Claro%20e%20Preto_Variacao%2003.jpg?psid=1&width=1292&height=862"
                },
                {
                    id: 2,
                    title: "Olá, sou o Leonardo Campelo",
                    description: "Sou Estudante!",
                    photo: "https://bn1303files.storage.live.com/y4m7Jqc2cei8lsPtx53bSwQSEgyO2dYA1pA56FPITgmSg9aZ2t8Ji0osa5MxN5NIuYNVGR6VXKEcYvNC4ETo_fERyndzgkk93DrYwmFteQH5tB01ZqMhUa-AAlJRc54GpuSRe5Hh9jHzFlv0fcXHJwxbHVufpPnlxQirvs9rZeMGVR2z3245Yt2YJHWBqvVM4dWSalUoVL7bP0PfLIrvjBOog/Cena%2007_Gebbwork_Escritorio%20Yaris_Carvalho%20Claro%20e%20Preto_Variacao%2003.jpg?psid=1&width=1292&height=862"
                },
            ],
        }
    },

    components: {
        ContactButton,
    },
}
</script>