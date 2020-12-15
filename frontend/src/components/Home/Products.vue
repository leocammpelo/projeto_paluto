<template>
    <el-container id="productsSection" class="products-container">
        <el-row class="products-titulos">
            <h4 class="subtitulo"> Produtos em destaque </h4>
            <h2 class="titulo"> NOSSO SHOWROOM </h2>
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
        padding: 5%;
        flex-direction: column !important;
        justify-content: center;
        max-width: $container-max-width;
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
                font-size: 30px;
                font-weight: bold;
                margin: 0;
                margin-bottom: 25px;           
            }
        
        }

        .product-estilo {
            margin-top: 40px;
            height: auto;
            width: 80% !important;
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
                    imagem: require("@/assets/escritorio.jpg"),
                    titulo: "Móveis para escritório",
                    descricao: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mollis et sagittis, nisl amet malesuada a. Lorem scelerisque amet nec sagittis fringilla massa. Morbi iaculis vitae aliquet purus. Tincidunt velit eleifend semper dolor nulla. Purus id cursus ultrices turpis. Metus, ultricies habitasse aliquam justo hendrerit turpis feugiat. Pharetra euismod eget egestas sociis rhoncus. Leo, turpis eget in egestas non adipiscing quis dolor vulputate. Commodo enim nibh feugiat imperdiet massa mi moles"
                },

                {
                    id: 1,
                    imagem: require("@/assets/escritorio.jpg"),
                    titulo: "Móveis para escritório",
                    descricao: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mollis et sagittis, nisl amet malesuada a. Lorem scelerisque amet nec sagittis fringilla massa. Morbi iaculis vitae aliquet purus. Tincidunt velit eleifend semper dolor nulla. Purus id cursus ultrices turpis. Metus, ultricies habitasse aliquam justo hendrerit turpis feugiat. Pharetra euismod eget egestas sociis rhoncus. Leo, turpis eget in egestas non adipiscing quis dolor vulputate. Commodo enim nibh feugiat imperdiet massa mi moles"
                },

                {
                    id: 2,
                    imagem: require("@/assets/escritorio.jpg"),
                    titulo: "Móveis para escritório",
                    descricao: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mollis et sagittis, nisl amet malesuada a. Lorem scelerisque amet nec sagittis fringilla massa. Morbi iaculis vitae aliquet purus. Tincidunt velit eleifend semper dolor nulla. Purus id cursus ultrices turpis. Metus, ultricies habitasse aliquam justo hendrerit turpis feugiat. Pharetra euismod eget egestas sociis rhoncus. Leo, turpis eget in egestas non adipiscing quis dolor vulputate. Commodo enim nibh feugiat imperdiet massa mi moles"
                },
            ],
        }
    },

    components: {
        CardProduct,
    },

}
</script>