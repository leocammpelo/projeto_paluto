<template>
    <el-container id="arqDecorSection" class="arqDecor">
        <el-row class="arqdecor-titulos">
               <h4 class="subtitulo">Arq & Decor</h4>
               <h2 class="titulo">STELLA MONTEIRO</h2>
        </el-row>
        <el-row class="arqdecor-img-texto">
            <el-col :xs="24" :sm="12" class="el-col-img">
                <img src="../../assets/Stella.png" alt="foto-Stella">
            </el-col>
            <el-col :xs="24" :sm="12" class="el-col-texto">
                <h4 class="texto-estilo">Arquiteta e Urbanista pelo Centro Universitário de Lavras (UNILAVRAS). 
                    Atualmente na área de Arquitetura de Interiores e também responsável 
                    pelo Visual Merchandising do showroom, com a criação de vitrines e 
                    ambientes únicos. Stella vem ao longo dos anos criando sua própria 
                    identidade sem abandonar o estilo minimalista. <br><br> Além de proporcionar 
                    uma seleção de móveis&decorações para uma infinidade de ambientes, o 
                    showroom disponibiliza um arquiteto para a realização de projetos 
                    arquitetônicos de interiores e também a fim de proporcionar uma 
                    consultoria exclusiva para os clientes na compra dos móveis.
                </h4>
                <div class="botao-estilo">
                    <ContactButton :title="titulo" :link="link" />
                </div>
            </el-col>
        </el-row>
    </el-container>
</template>

<style lang="scss">
    @import '../../styles/variables.scss';
    .arqDecor {
        padding: 5%;
        height: auto;
        flex-direction: column !important;
        justify-content: center;
        margin: 0 auto;
        background-image: url("../../assets/background-arq-decor.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;

        .arqdecor-titulos {
            padding: 0 7% 0 7%;

            .subtitulo {
                color: white;
                font-size: 24px;
                font-weight: 100;
                margin: 0;      
            }

            .titulo {
                font-size: 30px;
                font-weight: bold;
                margin: 0;
                margin-bottom: 25px;
                color: white;           
            }
        }

        @media screen and (max-width: 767px) {
            .arqdecor-titulos {

                .subtitulo {
                    font-size: 20px;
                }

                .titulo {
                    font-size: 26px;
                }
            }
        }

        .arqdecor-img-texto {
            padding: 0 5% 0 5%;

            .el-col-img {
                display: flex;
                justify-content: center;
                
                img {
                    height: 400px;
                    width: auto;
                }
            }

            .el-col-texto {
                justify-content: left;
                margin-top: 10px;

                .texto-estilo {
                    font-size: 16px;
                    font-style: normal;
                    font-weight: normal;
                    letter-spacing: 0.085em;
                    line-height: 126.19%;
                    color: white;
                }

                .botao-estilo {
                    display: flex;
                    justify-content: center;
                    margin-top: 30px;
                }
            }
        }

        @media screen and (max-width: 767px) {
            .arqdecor-img-texto {

               .el-col-texto {
                   margin-top: 20px;

                   .texto-estilo {
                       font-size: 12px;
                   }

                   .botao-estilo {
                       margin-bottom: 30px;
                   }
               } 
            }
        }
    }

</style>

<script>
import ContactButton from "../ContactButton"

export default {
    name: 'ArqDecor',

    data() {
        return {
            titulo: "SOLICITAR ACESSORIA",
            link: "https://api.whatsapp.com/send?phone=5535988792903",
        }
    },

    components: {
        ContactButton,
    }
}
</script>