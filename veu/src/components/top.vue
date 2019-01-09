<template>
    <div>
        <div :v-for="className in classnames"
             :class="className.name"
                 >

        </div>
    </div>
</template>

<script>
    export default {
        name: "top",
        data(){
           return{
            classNames:[
                {name:'wrapper row1'},
                {name:'wrapper row2'},
                {name:'wrapper bgded'}]
            }
        },
        methods: {

        }
    }
</script>

<style scoped>

</style>