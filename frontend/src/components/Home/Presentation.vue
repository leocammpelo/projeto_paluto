<template>
    <el-row id="presentation" justify="center" class="presentation-container">
        <el-main>
            <el-col class="presentation-video-description" :sm="24" :md="12">
                <h4 class="presentation-subtitulo">Sobre nós</h4>
                <h2 class="presentation-tittle"> DA NOSSA FAMÍLIA PARA SUA </h2>
                <p id="text-presentation"> {{videoDescription}} </p>
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
                margin: 0;
            }

            .presentation-tittle {
                color: #363435;
                font-size: 30px;
                margin: 0;
                margin-bottom: 25px;
            }

            p {
                font-size: 1.4em;
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

                h1 {
                    font-size: 3.5em;
                    text-align: center;
                }

                p {
                    font-size: 1em;
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
            videoDescription: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras odio pellentesque id maecenas congue magna. Elementum sed scelerisque tempor nibh posuere urna. Consectetur malesuada tortor nisl quisque et pellentesque mus bibendum. A, malesuada ac ipsum aliquam varius ut pulvinar. Hac convallis nunc ege",
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
            const ytComponentBounding = this.ytComponent.getBoundingClientRect();
            if(ytComponentBounding.top < window.innerHeight)
                this.player.playVideo();
            if(ytComponentBounding.top >= window.innerHeight || ytComponentBounding.top + ytComponentBounding.height <= 0)
                this.player.pauseVideo();
        },
    },

    created() {
        this.debouncedScroll = _.debounce(this.handleScroll, 150);
        window.addEventListener('scroll', this.debouncedScroll);   
    },

    mounted() {
        this.youTubeComponente = document.querySelector('youtube-video');

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
