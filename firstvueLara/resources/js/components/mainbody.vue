<template>
    <div>
        <wrapper-row1></wrapper-row1>
        <wrapper-row2></wrapper-row2>
        <wrapper-row3></wrapper-row3>
    </div>
</template>

<script>
    import wrapperRow1 from './wrapperRow1'
    import wrapperRow2 from './wrapperRow2'
    import wrapperRow3 from './wrapperRow3'

    export default {
        name:'mainBody',
        components:{
            wrapperRow1,
            wrapperRow2,
            wrapperRow3
        }
    }
</script>

<style>
    body {
        font-family: "Open Sans", Helvetica, Arial, sans-serif;
        overflow-x: hidden;
    }
    body {
        margin: 0;
        font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji";
        font-size: 1rem;
        font-weight: 400;
        line-height: 1.5;
        color: #212529;
        text-align: left;
        background-color: #fff;
    }
</style>
