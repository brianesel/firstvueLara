<template>
    <component
        :is="currentComponentTab">
    </component>
</template>

<script>
    import project1 from './proj1'
    import project2 from './proj2'
    import homepage from './homepage'
    import {eventBus} from "../app.js"

    export default {
        name: "wrapperRow2",
        data() {
            return {
                currentComponentTab: "homepage",
            }
        },
        components:{
            project1,
            project2,
            homepage
        },
        methods: {
            test(event) {
                console.log(event + "alo");
            }
        },
        created() {
            eventBus.$on('tab-clicked', currentComponentTab =>{this.currentComponentTab = currentComponentTab});
        }
    }
</script>

<style scoped>

</style>
