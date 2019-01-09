<template>
    <div>
        <img :src="brandImage"/>
        <h1>{{brandName}}</h1>
    </div>
</template>

<script>
    export default {
        name: "navBarBrand",
        data() {
            return {
                brandImage: 'https://s3-eu-central-1.amazonaws.com/centaur-wp/creativereview/prod/content/uploads/2013/05/be_0.jpg',
                brandName: 'EB'

            }
        },
        computed:{

        },
        components:{

        }

    }
</script>

<style scoped lang="scss" type="text/scss">
div{
    display: flex;
    border: solid 1px red;
    align-items: center;
    padding-top: .3125rem;
    padding-bottom: .3125rem;
    font-size: 1.25rem;
    line-height: inherit;
    white-space: nowrap;
    img{
        color: #656565;
        display: inline-block;
        width: 20%;
    }
    h1{

            display: flex;
            text-transform: uppercase;
            font-size: 5rem;
            color: #656565;
            letter-spacing: 1px;
            font-family: inherit;
            font-weight: 500;
            line-height: 1.2;
            margin-left:10px;

    }
}

</style>
