<template>
    <el-container id="partnersSection" class="parceiros">
        <el-row class="parceiros-titulos">
               <h4 class="titulo">Nossos parceiros</h4>
               <h2 class="subtitulo">QUEM TRABALHA AO NOSSO LADO</h2>
        </el-row>
        <el-row class="row-partners">
            <el-col class="col-img" :xs="12" :sm="6" :md="4" v-for="(item, i) in partnersCategory1" :key="i">
                <a :href="`${item.link}`" target="_blank">
                    <el-image :src="item.image" class="parceiros-imagens"></el-image>
                </a>
            </el-col>
        </el-row>
    </el-container>
</template>

<style lang="scss">
    @import '../../styles/variables.scss';
    
    .parceiros {
        display: flex;
        padding: 5%;
        flex-direction: column !important;
        justify-content: center;
        max-width: $container-max-width;
        background-color: white;
        margin: 0 auto;
        width: 100%;

        .parceiros-titulos {
            padding: 0 7% 0 7%;

            .titulo {
                color: #363435;
                font-size: 24px;
                font-weight: 100;
                margin: 0;  
            }

            .subtitulo {
                color: #363435;
                font-size: 30px;
                font-weight: bold;
                margin: 0;
                margin-bottom: 25px;      
            }
        }

        .row-partners {
            padding: 0 5% 0 5%;
            margin-top: 20px;
            align-items: center;
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            justify-content: center;

            .col-img {
                padding: 2%;
                text-align: center;

                .parceiros-imagens {
                    height: auto;
                    max-width: 200px;
                    filter: grayscale(1);
                    transition: all 1s;
                }

                .parceiros-imagens:hover {
                    filter: none;
                }
            }
        }

        @media screen and (max-width: 767px) {
            .parceiros-titulos {
                
                .titulo {
                    font-size: 15px;
                }

                .subtitulo {
                    font-size: 25px;
                }
            }

            .row-partners {
                .col-img {
                    padding: 7%;
                }

            }
        }
    }
</style>

<script>

export default {
    name: 'Partners',

    data()  {
        return {   
            partnersCategory1: [
                {
                    id: 0,
                    image: require("@/assets/logo_gebbwork.png"),
                    link: "https://www.gebbwork.com.br"
                },
                {
                    id: 1,
                    image: require("@/assets/logo_blume.png"),
                    link: "https://www.blumeimport.com"
                },
                {
                    id: 2,
                    image: require("@/assets/logo_plaxmetal.png"),
                    link: "https://www.plaxmetal.com.br"
                },
                {
                    id: 3,
                    image: require("@/assets/logo_rudnick.png"),
                    link: "https://www.rudnick.com.br"
                },
                {
                    id: 4,
                    image: require("@/assets/logo_kappesberg.png"),
                    link: "https://www.kappesberg.com.br"
                },
                {
                    id: 5,
                    image: require("@/assets/logo_lara.jpg"),
                    link: "https://www.laramoveis.com.br"
                },
                {
                    id: 6,
                    image: require("@/assets/logo_combinare.jpg"),
                    link: "https://www.combinare.com.br"
                },
                {
                    id: 7,
                    image: require("@/assets/logo_herval.jpg"),
                    link: "https://www.moveisherval.com.br"
                },
                {
                    id: 8,
                    image: require("@/assets/logo_vip.png"),
                    link: "https://www.vipestofados.com.br"
                },
            ],

        }
    },

}
</script>