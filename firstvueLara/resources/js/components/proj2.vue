<template>
    <div>
        <instagram-api></instagram-api>
    </div>
</template>

<script>
    import instagramApi from './instagramApi';
    export default {
        name: "proj2",
        components: {
            instagramApi
        },
        data(){
            
        }
    }
</script>

<style scoped>
div{display: flex;}
</style>
