<template>
    <el-row id="presentation" justify="center" class="presentation-container">
        <el-main>
            <el-col class="presentation-video-description" :sm="24" :md="12">
                <h4 class="presentation-subtitulo">Sobre nós</h4>
                <h2 class="presentation-tittle"> DA NOSSA FAMÍLIA PARA SUA </h2>
                <p id="text-presentation"> <b> {{ videoDescription1 }} </b> <br><br> {{ videoDescription2 }} </p>
            </el-col>
            <el-col class="youtube-video" align="center" :sm="24" :md="12">
                <youtube id="youtube-video" :video-id="video_id" :mute="true" @ready="ready"></youtube>
            </el-col>
        </el-main>
    </el-row>
</template>

<style lang="scss">
    @import '../../styles/variables.scss';
    
    @keyframes fadeIn {
        from {
        opacity: 0;
        }
        to{
            opacity: 1;
        }
    }
    @-moz-keyframes fadeIn {
        from {
        opacity: 0;
        }
        to{
        opacity: 1;
         }
    }
    @-webkit-keyframes fadeIn {
        from {
        opacity: 0;
        }
        to{
            opacity: 1;
        }
    }
    .efeito-text{
        animation-iteration-count: 1;
        -moz-animation: fadeIn 2s ease-out !important;
        animation: fadeIn 2s ease-out !important;
        -webkit-animation: fadeIn 2s ease-out !important;
    }
    .presentation-container {
        padding: 5%;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100%;
        min-height: 50vh;
        background-color: $secondary-background-color;
        

        .el-main {
            max-width: $container-max-width;
            display: flex;
            flex-wrap: wrap;
            padding-top: 3%; 
            padding-bottom: 3%;
        }

        .presentation-video-description {
            padding: 0 5% 0 5%;
            font-weight: 300 !important;

            .presentation-subtitulo {
                color: #363435;
                font-size: 24px;
                font-weight: 100;
                margin: 0;                }

            .presentation-tittle {
                font-size: 30px;
                font-weight: bold;
                margin: 0;
                margin-bottom: 25px;    
            }

            p {
                font-size: 16px;
            }

        }

        .youtube-video {

            #youtube-video {
                display: flex;
                align-items: center;

                iframe {
                    display: flex;
                    width: 100%;
                }    
            }
        }

        @media screen and (max-width: 1024px) {
            .el-main {
                padding-top: 8%; 
                padding-bottom: 8%;
            }

            .presentation-video-description {

                .presentation-subtitulo {
                    font-size: 20px;
                }

                .presentation-tittle {
                    font-size: 26px;
                }

                p {
                    font-size: 14px;
                    text-align: center;
                }
            } 
        }
    }
</style>

<script>
import Vue from 'vue'
import _ from 'lodash'
import VueYoutubeEmbed from 'vue-youtube-embed'

Vue.use(VueYoutubeEmbed)

export default {
    name: 'Presentation',
    
    data() {
        return {
            videoDescription1: "Paluto Móveis - SEU AMBIENTE EM BOAS MÃOS",
            videoDescription2: "Em meio a Pandemia, surge a Paluto Móveis com o objetivo de lhe atender de forma exclusiva, com produtos de alta qualidade e requinte. Seu fundador, Paulo Vinicius, vem de uma família de tradição no ramo moveleiro, e entende de móveis há mais de 25 anos. Nossa o proposta é oferecer a solução ideal para seu ambiente, para isso contamos com a TALENTOSA arquiteta Stella Monteiros, para auxiliar desde a elaboração do seu projeto até a escolha definitiva dos móveis e decorações",
            video_id: "64YeMgImYQE",
            
            player: {},
            youTubeComponente: {},
        }
    },

    methods: {
        ready(event) {
            this.player = event.target;
        },

        handleScroll() {
            const youTubeComponenteBounding = this.youTubeComponente.getBoundingClientRect();
            if(youTubeComponenteBounding.top < window.innerHeight)
                this.player.playVideo();
            if(youTubeComponenteBounding.top >= window.innerHeight || youTubeComponenteBounding.top + youTubeComponenteBounding.height <= 0)
                this.player.pauseVideo();
        },
    },

    created() {
        this.debouncedScroll = _.debounce(this.handleScroll, 150);
        window.addEventListener('scroll', this.debouncedScroll);   
    },

    mounted() {
        this.youTubeComponente = document.querySelector('.youtube-video');

        window.addEventListener('scroll', () => {
            const scrolled = window.scrollY;
            const position = document.getElementById("text-presentation").offsetTop;
            if(scrolled >=position){
                setEfect();
            }
        });
    },

    beforeDestroy() {
        window.removeEventListener('scroll', this.debouncedScroll);
    }
    
}

function setEfect() {
    document.getElementById("text-presentation").className = "efeito-text";
}

</script>
