<template>
    <div class="hah">
        <heading :level="1">Hello world!</heading>
        <heading :level="1">Hello world!</heading>
        <heading :level="1">Hello world!</heading>
        <heading :level="1">Hello world!</heading>
        <heading :level="1">Hello world!</heading>
        <heading :level="1">Hello world!</heading>


    </div>
</template>

<script>
    import Vue from 'vue'
    export default {
        name: "NavBar",

    }

Vue.component('heading',{
    render: function (createMenu) {
        return createMenu('h'+this.level,
            this.$slots.default)
    },
    props: {
        level: {
            type: Number,
            required: true
        }
    }
})
</script>

<style>
    .hah {display: block}
heading {
    display: block;
    border: solid red 10px;
    background-color: aqua;
}
</style>