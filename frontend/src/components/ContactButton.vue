<template>
    <div> 
        <b-button class="contato-button" v-b-modal.modal-1>CONTATE-NOS</b-button>

        <b-modal id="modal-1" title="BootstrapVue">
            <p class="my-4">Hello from modal!</p>
        </b-modal>

    </div>
</template>

<style lang="scss">
    .contato-button {
        font-family: Roboto;
        font-size: 0.9em !important;
        font-weight: 700 !important;
        width: 200px;
        padding-top: 8px !important;
        padding-bottom: 8px !important;
        border-width: 2px !important;
        color: #fff !important;
        border-color:#f0f0f0 !important; 
        background: transparent !important;
    }

    .contato-button:hover {
        background: linear-gradient(270deg, #C68953 0%, #F3AF73 31.77%, #D8965C 100%) !important;
    }

</style>

<script>
export default {
    name: 'ContactButton',

    methods: {
        
    },
}
</script>