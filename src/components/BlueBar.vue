<script>
    export default{
        data(){
            return{
                merch: [
                    {
                        logoMerch: "../assets/img/buy-comics-digital-comics.png",
                        merchName: "DIGITAL COMICS",
                        alt: "digital comics logo",
                    },
                    {
                        logoMerch: "../assets/img/buy-comics-merchandise.png",
                        merchName: "DC MERCHANDISE",
                        alt: "dc merchandise logo",
                    },
                    {
                        logoMerch: "../assets/img/buy-comics-subscriptions.png",
                        merchName: "SUBSCRIPTION",
                        alt: "subscription logo",
                    },
                    {
                        logoMerch: "../assets/img/buy-comics-shop-locator.png",
                        merchName: "COMIC SHOP LOCATOR",
                        alt: "comic shop locator logo"
                    },
                    {
                        logoMerch: "../assets/img/buy-dc-power-visa.svg",
                        merchName: "DC POWER VISA",
                        alt: "dc power visa logo"
                    }
                ]
            }
        },
        methods: {
            imgPath: function(img){
                return new URL(`${img}`, import.meta.url).href
            }
        }
    }
</script>

<template>
    <div class="blue-container">
        <div class="big-merch-container">
            <div class="merchbox text-white d-flex align-items-center gap-3" v-for="singleMerch in merch">
                <div class="logo-merch-cont">
                    <img :src="imgPath(singleMerch.logoMerch)" alt="" class="logo-merch-item">
                </div>
                <a href="#">{{singleMerch.merchName}}</a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../styles/partials/variables";
    @use "../styles/partials/mixins";

    .blue-container{
        background-color: variables.$color-primary;
    };

    .big-merch-container{
        @include mixins.centered-content;
        padding-top: 3rem;
        padding-bottom: 3rem;

        a {
            color: white;
            text-decoration: none;
        }
    };

    .logo-merch-item{
        width: 50px;
    }




</style>