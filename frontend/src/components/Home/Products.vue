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
        background-color: $secondary-background-color;
        margin: 0 auto;
        width: 100%;

        .products-titulos {
            padding: 0 7% 0 7%;

            .subtitulo {
                color: #363435;
                font-size: 24px;
                font-weight: 100;
                margin: 0;          
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
                    titulo: "Móveis para escritório",
                    descricao: "É cada vez mais comum as pessoas trocarem os ambientes corporativos para executarem suas atividades profissionais em casa. Assim, o ambiente doméstico precisa se adaptar aos novos tempos e tornar-se mais flexível, mas sem perder a elegância. O escritório não precisa ser sinônimo de ambiente burocrático ou improvisado. Cada vez mais pessoas separam um cantinho da casa para o home office e, para o trabalho render, ele precisa ser um espaço confortável, organizado, agradável e bonito."
                },

                {
                    id: 1,
                    imagem: require("@/assets/casa.png"),
                    titulo: "Móveis para sala",
                    descricao: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mollis et sagittis, nisl amet malesuada a. Lorem scelerisque amet nec sagittis fringilla massa. Morbi iaculis vitae aliquet purus. Tincidunt velit eleifend semper dolor nulla. Purus id cursus ultrices turpis. Metus, ultricies habitasse aliquam justo hendrerit turpis feugiat. Pharetra euismod eget egestas sociis rhoncus. Leo, turpis eget in egestas non adipiscing quis dolor vulputate. Commodo enim nibh feugiat imperdiet massa mi moles"
                },

                {
                    id: 2,
                    imagem: require("@/assets/decoracao.png"),
                    titulo: "Decoração",
                    descricao: "Para você se inspirar, separamos ideias de projetos que fogem do óbvio, com um décor lindo. O ambiente pode ser flexível, multiuso e com alguns truques, otimizar espaço e tornar o ambiente super inspirador."
                },
            ],
        }
    },

    components: {
        CardProduct,
    },

}
</script>