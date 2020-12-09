<template>
    <b-container>

        <b-navbar class="navbar-style" toggleable="lg">
            <b-navbar-brand href="#">
                <img class="logo-style" src="../assets/logo.png" alt="Logo">
            </b-navbar-brand>
            
            <b-navbar-nav class="ml-auto"> 
                <b-nav-item class="secao-style">Sobre Nós</b-nav-item>
                <b-nav-item>Equipe</b-nav-item>
                <b-nav-item>Produtos</b-nav-item>
                <b-nav-item>Contatos</b-nav-item>
                <b-nav-item href="https://github.com/vuejs-templates/webpack/issues/121" target="_blank">
                    <img class="whatsapp-style" src="../assets/whatsapp.png" alt="Instagram">
                </b-nav-item>
                <b-nav-item href="https://github.com/vuejs-templates/webpack/issues/121" target="_blank">
                    <img class="instagram-style" src="../assets/instagram.png" alt="Instagram">
                </b-nav-item>
            </b-navbar-nav>

        </b-navbar>
    
    </b-container>
</template>

<style lang="scss" scoped>
    .container {
        max-width: 100% !important;
        padding: 0px !important;
        font-family: Roboto;
        letter-spacing: 0.05em;

        .navbar-style {
            background-color: #7B2D33;

            .logo-style {
                height: 50px;
                margin-left: 80px;
            }

            .whatsapp-style {
                height: 22px;
                width: 22px;
            }

            .instagram-style {
                height: 22px;
                width: 22px;
            }           
        }
    }
</style>