<template>
    <el-row id="productsSection" justify="center" class="products-container">
        <el-main>
            <el-row class="products-titulos">
                <h4 class="subtitulo"> Nossa equipe </h4>
                <h2 class="titulo"> A FAMÍLIA QUE ESCOLHEMOS </h2>
            </el-row>
        </el-main>
    </el-row>
</template>

<style lang="scss">
@import '../../styles/variables.scss';
    
    .products-container {
        display: flex;
        padding: 5%;
        flex-direction: column !important;
        justify-content: center;
        background-color: $secondary-background-color;
        height: 100%;

        .el-main {
            max-width: $container-max-width;
            display: grid;
            flex-wrap: wrap;

            .subtitulo {
                padding: 0 5% 0 5%;
                font-weight: 300 !important;               
            }

            .titulo {
                color: #363435;
                font-size: 30px;
                padding: 0 5% 0 5%;
                margin: 0;
                margin-bottom: 25px;                
            }
        }
    }
</style>


<script>


export default {
    
}
</script>