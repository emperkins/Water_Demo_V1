<template>
    <div class="spinner">
        <img src="../assets/loading.svg" alt="loading"/>
    </div>
</template>

<script>
    import Auth from './../auth/AuthService';
    const auth = new Auth();
    export default {
        name: '',
        mounted() {
            this.$nextTick(() => {
                auth.handleAuthentication();
            });
        },
    };
</script>

<style>
    .spinner {
        position: absolute;
        display: flex;
        justify-content: center;
        height: 100vh;
        width: 100vw;
        background-color: white;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
    }
</style>
