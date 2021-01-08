<template>
    <el-container id="productsSection" class="products-container">
        <el-row class="products-titulos">
            <h4 class="subtitulo"> Produtos em destaque </h4>
            <h2 class="titulo"> SOB NOSSO OLHAR </h2>
        </el-row>
        <el-row class="max-width-container product-estilo">
            <el-col :xs="24" :sm="8"
                v-for="item in products"
                v-bind:todo="item"
                v-bind:key="item.id">
                <CardProduct
                    :image="item.imagem"
                    :title="item.titulo"
                    :description="item.descricao"
                    :link="item.link"
                />
            </el-col>
        </el-row>
    </el-container>
</template>

<style lang="scss">
    @import '../../styles/variables.scss';
    
    .products-container {
        display: flex;
        padding: 0 5% 0 5%;
        flex-direction: column !important;
        justify-content: center;
        max-width: $container-max-width;
        background-color: #F9F9F9;
        margin: 0 auto;
        width: 100%;

        .products-titulos {
            padding: 0 7% 0 7%;

            .subtitulo {
                color: #363435;
                font-size: 24px;
                font-weight: 100;
                margin: 0;
                margin-top: 30px;          
            }

            .titulo {
                color: #363435;
                font-size: 30px;
                font-weight: bold;
                margin: 0;
                margin-bottom: 25px;           
            }
        
        }

        .product-estilo {
            margin-top: 15px;
            height: auto;
            width: 80% !important;
            margin-bottom: 50px;
        }
    }

    @media screen and (max-width: 1024px) {
        .products-container {
            padding: 5%;
            

            .products-titulos {

                .titulo {
                    margin-bottom: 5px;           
                }
            
            }
            
            .product-estilo {
                margin-top: 40px;
                height: auto;
                width: 80% !important;

                .el-col {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }
            }
        }       
    }

</style>


<script>
import CardProduct from '../Products/CardProduct.vue'

export default {
    name: 'Products',

    data() {
        return {
            products: [
                {
                    id: 0,
                    imagem: require("@/assets/escritorio.png"),
                    titulo: "Corporativo (Escritórios)",
                    descricao: "ADOTE BOAS ESTRATÉGIAS NO SEU ESPAÇO, PARA TRAZER BONS RESULTADOS",
                    link: "https://photos.app.goo.gl/HQuUNBYWrg7UhDen8"
                },

                {
                    id: 1,
                    imagem: require("@/assets/casa.png"),
                    titulo: "Casa",
                    descricao: "CUIDAR DA CASA É CUIDAR DE VOCÊ",
                    link: "https://photos.app.goo.gl/E7ktaD5NvV83NWyY6"
                },

                {
                    id: 2,
                    imagem: require("@/assets/decoracao.png"),
                    titulo: "Decoração",
                    descricao: "DECORAR É A ARTE DE CONECTAR PESSOAS E ESPAÇOS",
                    link: "https://photos.app.goo.gl/6uwA6HNeZ8yHSL657"
                },
            ],
        }
    },

    components: {
        CardProduct,
    },

}
</script>