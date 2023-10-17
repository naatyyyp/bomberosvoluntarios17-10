<template>
    <div>
        <login-component v-if="!user" @logueado="logueado"/>
        <admin-component></admin-component>
    </div>
</template>

<script>
    import LoginComponent from './components/LoginComponent.vue'

    export default {
        name: 'AdminPage',
        components: {
            LoginComponent
        },
        data: () => ({
            user: null
        }),
        methods: {
            logueado(payload){
                this.user = payload
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>