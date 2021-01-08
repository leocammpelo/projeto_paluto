<template>
    <div> 
        <el-button class="contato-button" @click="navigateTo()">CONTATE-NOS</el-button>
    </div>
</template>

<style lang="scss">
    .contato-button {
        font-family: Roboto;
        font-size: 0.9em !important;
        width: 200px;
        border-radius: 0 !important;
        color: #fff !important;
        background: linear-gradient(270deg, #C68953 0%, #F3AF73 31.77%, #D8965C 100%) !important;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.15), 0px 0px 10px rgba(234, 167, 107, 0.25) !important;
    }

    .contato-button:hover {
        background: transparent !important;
    }

</style>

<script>
export default {
    name: 'ContactButton',

    methods: {
         navigateTo() {
             window.location.href = "http://localhost:8080/#/";
        }       
    },
}
</script>