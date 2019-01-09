<template>
    <div class="col-12">
        <nav class="navbar navbar-expand-xl navbar-light bg-light">
            <nav-bar-brand></nav-bar-brand>
            <menu-bar></menu-bar>
        </nav>
    </div>
</template>

<script>
    import navBarBrand from './navBarBrand'
    import menuBar from './menuBar'

    export default {
        name: "wrapperRow1",
        components:{
            navBarBrand,
            menuBar
        }
    }
</script>

<style>
    .navbar {
        height: 100px;
        padding-left: 20px;
        padding-right: 20px;
        margin-top: 50px;
        display: flex;
        allign-items:center;
    }
    menu-bar{
        display: flex;
    }
    nav-bar-brand{
        display: flex;
        margin-left: 75%;
    }
    .bg-light {
        background-color: #f8f9fa!important;
    }

</style>
