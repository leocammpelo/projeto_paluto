<template>
    <div class="flip-card"> 
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <el-card class="card-item" :body-style="{ padding: '0px' }">
                    <div class="figure">
                        <img :src="image" />
                    </div>
                    <div style="padding: 14px;">
                        <p class="title-style"> <b> {{ title }} </b> </p>
                        <p>Saiba mais <img :src="iconeMais" class="iconeMais-style"> </p>
                    </div>
                </el-card>
            </div>
            <div class="flip-card-back">
                <p class="description"> {{ excerpt }} </p>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
@import '../../styles/variables.scss';
    .flip-card {
        height: 430px;
        margin: 20px;
        width: 93%;
        background-color: transparent;

        .flip-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.8s;
            transform-style: preserve-3d;


            .flip-card-front {
                background-color: transparent;
                color: black;

                .card-item {
                    height: 430px;

                    .figure {
                        position: relative;
                        height: 300px;
                        width: 100%;
                        margin: 0;
                    }

                    .figure img {
                        position: absolute;
                        opacity: 1;
                        top: 50%;
                        left: 50%;
                        height: 100%;
                        width: 100%;
                        -webkit-transform: translate(-50%,-50%);
                            -ms-transform: translate(-50%,-50%);
                                transform: translate(-50%,-50%);            
                    }

                    .figure img.portrait {
                        width: 100%;
                        height: auto;        
                    }

                    .title-style {
                        margin-top: 15px;
                        margin-bottom: 0px;
                        font-size: 20px;
                        font-weight: bold;
                        color: $secondary-font-color;
                    }

                    .description {
                        align-items: left;
                        justify-content: left;
                        font-size: 15px;
                        color: $secondary-font-color;       
                    }

                    p {
                        margin-top: 15px;
                        display: flex;
                        align-items: center;
                        justify-content: center;
  
                        .iconeMais-style {
                            margin-left: 5px;
                            height: 13px;
                            display: flex;
                            opacity: 0.8;
                        }


                    }
                    
                }

                .card-item:hover {
                    border: 0.5px solid #7B2D33;
                }
            }
        
            .flip-card-back {
                background-color: #FEFEFE;
                color: #000000;
                transform: rotateY(180deg);

                p {
                    font-size: 14px;
                    padding: 4%;
                }
            }

            .flip-card-front, .flip-card-back {
                position: absolute;
                width: 100%;
                height: 100%;
                -webkit-backface-visibility: hidden;
                backface-visibility: hidden;
            }
        }
    }

    .flip-card:hover .flip-card-inner {
        transform: rotateY(180deg);
    }

    @media screen and (max-width: 1024px) {
        .flip-card {
            margin-top: 10px;
            height: 315px !important;


            .flip-card-inner {

                .flip-card-front {

                    .card-item {
                        height: 100%;

                        .figure {
                            height: 200px;
                        }

                        .title-style {
                            font-size: 15px;
                        }

                        
                    }
                }
                
                .flip-card-back {
                    height: 100%;

                    p {
                        font-size: 10px;
                    }
                }
            }
        }
    }

</style>

<script>
export default {
    name: 'CardProduct',

    props: {
        id: Intl,
        image: String,
        title: String,
        description: String
    },

    data() {
        return {
            iconeMais: require("@/assets/iconeMais.png"),
            excerpt: "",
        };
    },

    created() {
        let text = this.description;
        if(text.length >500) { 
            text = text.slice(0,500);
            this.description = text +"...";
        }

        this.excerpt = this.description;
        if (this.excerpt.length > 500) {
            this.excerpt = this.excerpt.slice(0, 500) + "...";
        }       
    }
}
</script>