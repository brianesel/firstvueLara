<template>
    <div class="product">

        <div class="product-image">
            <img :src="productimage" />
        </div>

        <div class="product-info">
            <h1>{{ product }}</h1>

            <ul>
                <ol v-for="detail in details">{{ detail }}</ol>
            </ul>
                <div>
                   <img class="platform-image"
                    :v-for="(platform, index) in platforms"
                    :src="platform.platformImage"
                    @mouseover="updateProduct(index)"
                   >
                </div>


            <div class="cart">
                <p>Cart({{ cart }})</p>
            </div>

        </div>

    </div>


</template>

<script>
    export default {
        name: "product",
        data() {
            return {
                productname: "First Game",
                developer: "BE",
                selectedPlatform: 0,
                details: ['95% self-developed', 'the rest was extracted from others brains','9 in 10 case brain dead'],
                platforms: [
                    {
                        platformId: 2234,
                        platformGame: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSK41jpWhPsUgjyg7Scx9mjjD_jLqYbAPM_SJVwG2eJqKAczru6Ig',
                        platformImage: 'https://images.unsplash.com/photo-1484068043587-e86f6124d2ee?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&w=1000&q=80',
                        platformQuantity: 10
                    },
                    {
                        platformId: 2235,
                        platformGame: 'https://images.techhive.com/images/article/2015/10/invisible-inc-100622096-orig.jpg',
                        platformImage: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Penguins_walking_-Moltke_Harbour%2C_South_Georgia%2C_British_overseas_territory%2C_UK-8.jpg/220px-Penguins_walking_-Moltke_Harbour%2C_South_Georgia%2C_British_overseas_territory%2C_UK-8.jpg',
                        platformQuantity: 10
                    },
                    {
                        platformId: 2236,
                        platformGame: 'https://i.ytimg.com/vi/gB13a1J4zIk/maxresdefault.jpg',
                        platformImage: 'data:image/jpeg;base64,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',
                        platformQuantity: 10
                    }
                ],
                cart: 0
            }
        },
        methods: {
            updateProduct: function(index) {
                this.selectedPlatform = index
            }

        },
        computed:{
            title(){
                return this.developer+' '+this.productname
            },
            productimage(){
                return this.platforms[this.selectedPlatform].platformGame
            }
        }

    }
</script>

<style>
    .product-image {
        display:inline;
    }
    .product-info {
        margin-top: 10px;
        flex-basis: 500px;
        text-align: center;
    }
    .platform-image {
        width: 40px;
        height: 40px;
        margin-top: 5px;
    }
    img {
        border: 1px solid #d8d8d8;
        width: 30%;
        margin: 40px;
        box-shadow: 0px .5px 1px #d8d8d8;
    }
</style>