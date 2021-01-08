<template>
    <el-container id="contactSection" class="contact">
        <el-row>
            <el-col :xs="24" :sm="12" class="el-col-map">
                <h3 class="titulo-map">LOCALIZAÇÃO</h3>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d29746.55375329105!2d-45.00408292106422!3d-21.25882809593379!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94caada15fd8ae53%3A0x58112f827d649135!2sPaluto%20M%C3%B3veis!5e0!3m2!1spt-BR!2sbr!4v1609958381954!5m2!1spt-BR!2sbr" width="100%" height="350px" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
            </el-col>
            <el-col :xs="24" :sm="12" class="el-col-infos">
                <div class="infos-style">
                    <h3 class="titulo-infos">CONTATOS</h3>
                    <p> <img class="icone-estilo" src="../../assets/localizacao.png" alt="ícone-localização"> {{ informacoes.endereco }} </p>
                    <p> <img class="icone-estilo" src="../../assets/telefone.png" alt="ícone-localização"> {{ informacoes.telefone }} </p>
                    <p> <img class="icone-estilo" src="../../assets/email.png" alt="ícone-localização"> {{ informacoes.email }} </p>
                    <p> <img class="icone-estilo" src="../../assets/horarios.png" alt="ícone-localização"> {{ informacoes.horario }} </p>
                    <div class="links-logo-estilo">
                        <div class="links-estilo">
                            <p> <a href="https://github.com/vuejs-templates/webpack/issues/121" target="_blank"> <svg class="whatsapp-style" height="682pt" viewBox="-23 -21 682 682.66669" width="682pt" xmlns="http://www.w3.org/2000/svg"><path d="m544.386719 93.007812c-59.875-59.945312-139.503907-92.9726558-224.335938-93.007812-174.804687 0-317.070312 142.261719-317.140625 317.113281-.023437 55.894531 14.578125 110.457031 42.332032 158.550781l-44.992188 164.335938 168.121094-44.101562c46.324218 25.269531 98.476562 38.585937 151.550781 38.601562h.132813c174.785156 0 317.066406-142.273438 317.132812-317.132812.035156-84.742188-32.921875-164.417969-92.800781-224.359376zm-224.335938 487.933594h-.109375c-47.296875-.019531-93.683594-12.730468-134.160156-36.742187l-9.621094-5.714844-99.765625 26.171875 26.628907-97.269531-6.269532-9.972657c-26.386718-41.96875-40.320312-90.476562-40.296875-140.28125.054688-145.332031 118.304688-263.570312 263.699219-263.570312 70.40625.023438 136.589844 27.476562 186.355469 77.300781s77.15625 116.050781 77.132812 186.484375c-.0625 145.34375-118.304687 263.59375-263.59375 263.59375zm144.585938-197.417968c-7.921875-3.96875-46.882813-23.132813-54.148438-25.78125-7.257812-2.644532-12.546875-3.960938-17.824219 3.96875-5.285156 7.929687-20.46875 25.78125-25.09375 31.066406-4.625 5.289062-9.242187 5.953125-17.167968 1.984375-7.925782-3.964844-33.457032-12.335938-63.726563-39.332031-23.554687-21.011719-39.457031-46.960938-44.082031-54.890626-4.617188-7.9375-.039062-11.8125 3.476562-16.171874 8.578126-10.652344 17.167969-21.820313 19.808594-27.105469 2.644532-5.289063 1.320313-9.917969-.664062-13.882813-1.976563-3.964844-17.824219-42.96875-24.425782-58.839844-6.4375-15.445312-12.964843-13.359374-17.832031-13.601562-4.617187-.230469-9.902343-.277344-15.1875-.277344-5.28125 0-13.867187 1.980469-21.132812 9.917969-7.261719 7.933594-27.730469 27.101563-27.730469 66.105469s28.394531 76.683594 32.355469 81.972656c3.960937 5.289062 55.878906 85.328125 135.367187 119.648438 18.90625 8.171874 33.664063 13.042968 45.175782 16.695312 18.984374 6.03125 36.253906 5.179688 49.910156 3.140625 15.226562-2.277344 46.878906-19.171875 53.488281-37.679687 6.601563-18.511719 6.601563-34.375 4.617187-37.683594-1.976562-3.304688-7.261718-5.285156-15.183593-9.253906zm0 0" fill-rule="evenodd"/></svg> </a> Whatsapp </p>
                            <p> <a href="https://github.com/vuejs-templates/webpack/issues/121" target="_blank"> <svg data-v-41be6633="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="instagram" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="instagram-style bi-instagram mx-auto b-icon bi"><g data-v-41be6633=""><path d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"></path></g></svg> </a> Instagram </p>
                        </div>
                        <div class="logo-estilo"> 
                            <img src="../../assets/logomarca.png" alt="logo-marca"> 
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>
    </el-container>
</template>

<style lang="scss">
    @import '../../styles/variables.scss';
    
    .contact {
        display: flex;
        padding: 5%;
        justify-content: center;
        max-width: $container-max-width;
        margin: 0 auto;
        background-color: #363435;

        .el-row {
            margin-top: 30px;
            width: 80%;

            .el-col-map {

                .titulo-map {
                    font-size: 24px;
                    font-weight: bold;
                    margin: 0;
                    margin-bottom: 25px;
                    letter-spacing: 0.085em;
                    color: white;     
                }
            }

            .el-col-infos {
                justify-content: center;

                .infos-style {
                    margin-left: 80px;
                
                    .titulo-infos {
                        font-size: 24px;
                        font-weight: bold;
                        margin: 0;
                        margin-bottom: 25px;
                        letter-spacing: 0.085em;
                        color: white;    
                    }

                    p {
                        height: auto;
                        width: 100%;
                        font-size: 15px;
                        color: white;
                    }

                    .icone-estilo {
                        height: 20px;
                        width: 20px;
                    }

                    .links-logo-estilo {
                        height: auto;
                        width: 100%;

                        .links-estilo {
                            justify-content: center;
                            align-items: center;
                            margin-top: 30px;

                            .whatsapp-style {
                                height: 20px;
                                width: 20px;
                                fill: white;
                            }

                            .whatsapp-style:hover {
                                -webkit-transform: scale(0.8);
                                -ms-transform: scale(0.8);
                                transform: scale(0.8);
                                fill: #D8965C;
                            }

                            .instagram-style {
                                height: 20px;
                                width: 20px;
                                margin-right: 80px;
                                fill: white;
                            }

                            .instagram-style:hover {
                                -webkit-transform: scale(0.8);
                                -ms-transform: scale(0.8);
                                transform: scale(0.8);
                                fill: #D8965C;
                            }
                        }

                        .logo-estilo {
                            display: grid;
                            height: 100px;
                            justify-content: right;

                            img {
                                height: 100%;
                            }
                        }
                    }
                }
            }

            @media screen and (max-width: 767px) {
                .el-col-infos {
                    justify-content: center;

                    .infos-style {
                        margin-top: 40px;
                        margin-left: 0px;

                        p {
                            font-size: 12px;
                        }
                        .icone-estilo {
                            height: 10px;
                            width: 10px;
                        }

                        .links-logo-estilo {

                            .links-estilo {
                                .whatsapp-style {
                                    height: 15px;
                                    width: 15px;
                                }

                                .instagram-style {
                                    height: 15px;
                                    width: 15px;                                   
                                }
                                
                            }

                            .logo-estilo {
                                height: 70px;
                            }
                        }                        
                    }
                }
            }

        }
        
    }

</style>

<script>

export default {
    name: 'Contact',

    data() {
        return {
            informacoes: {
                endereco: 'Rua Otacílio Negrão De Lima, 177, Centro - Lavras - MG',
                telefone: '(35) 3826-2904',
                email: 'palutomoveis@palutomoveis.com.br',
                horario: 'Segunda a Sexta - 08:30 às 18:00hrs Sábado - 08:30 à 12:00hrs',
            }
        }
    },

}
</script>