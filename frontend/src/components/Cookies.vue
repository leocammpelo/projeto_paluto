<template>

</template>

<script>
    export default {
    data() {
        return {
            status: null,
        }
    },

    methods: {
        cookieStatus (status) {
        console.log('status: ' + status)
        this.status = status
        },
        cookieClickedAccept () {
        console.log('here in accept')
        this.status = 'accept'
        },
        cookieClickedDecline () {
        console.log('here in decline')
        this.status = 'decline'
        },
    },

    computed: {
        statusText () {
            return this.status || 'No cookie set'
        }
    }
}
    
</script>