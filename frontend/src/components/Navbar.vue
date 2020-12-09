<template>
    <b-container>

        <b-navbar class="navbar-style" toggleable="lg">

            <b-navbar-brand href="#">
                <img class="logo-style" src="../assets/logo.png" alt="Logo">
            </b-navbar-brand>
            
            <b-navbar-toggle target="navbar-toggle-collapse"></b-navbar-toggle>
            
            <b-collapse id="navbar-toggle-collapse" is-nav>
                <b-navbar-nav class="ml-auto"> 
                    <b-nav-item> <font class="item-style"> Sobre Nós </font> </b-nav-item>
                    <b-nav-item> <font class="item-style"> Equipe </font> </b-nav-item>
                    <b-nav-item> <font class="item-style"> Produtos </font> </b-nav-item>
                    <b-nav-item> <font class="item-style"> Contatos </font> </b-nav-item>
                    <b-nav-item href="https://github.com/vuejs-templates/webpack/issues/121" target="_blank">
                        <img class="whatsapp-style" src="../assets/whatsapp.png" alt="Instagram">
                    </b-nav-item>
                    <b-nav-item href="https://github.com/vuejs-templates/webpack/issues/121" target="_blank">
                        <img class="instagram-style" src="../assets/instagram.png" alt="Instagram">
                    </b-nav-item>
                </b-navbar-nav>
            </b-collapse>

        </b-navbar>
    
    </b-container>
</template>

<style lang="scss" scoped>
    .container {
        max-width: 100% !important;
        padding: 0px !important;

        .navbar-style {
            background-color: #7B2D33;

            .logo-style {
                height: 50px;
                margin-left: 80px;
            }
            .logo-style:hover {
                -webkit-transform: scale(0.8);
                -ms-transform: scale(0.8);
                transform: scale(0.8);
            }

            .item-style {
                font-family: Roboto;
                font-style: normal;
                letter-spacing: 0.05em;
                margin-left: 5px;
                margin-right: 5px;
                color: #FEFEFE;
            }

            .item-style:hover {
                color: #B38F6F;
            }

            .whatsapp-style {
                height: 22px;
                width: 22px;
                margin-left: 20px;
            }

            .instagram-style {
                height: 22px;
                width: 22px;
                margin-right: 80px;
            }           
        }

        @media screen and (max-width:767px) {

            .navbar-style {

                .logo-style {
                    height: 25px;
                    margin-left: 20px;
                }

                .item-style {
                    margin-left: 2px;
                    margin-right: 2px;
                }

                .whatsapp-style {
                    height: 12px;
                    width: 12px;
                    margin-left: 2px;
                }

                .instagram-style {
                    height: 12px;
                    width: 12px;
                    margin-left: 2px;
                }           
            }
        }

        @media screen and (max-width:991px) {

            .navbar-style {

                .logo-style {
                    height: 35px;
                    margin-left: 20px;
                }

                .item-style {
                    margin-left: 2px;
                    margin-right: 2px;
                }

                .whatsapp-style {
                    height: 15px;
                    width: 15px;
                    margin-left: 2px;
                }

                .instagram-style {
                    height: 15px;
                    width: 15px;
                    margin-left: 2px;
                }           
            }
        }
    }
</style>