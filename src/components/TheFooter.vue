<script>
export default{
    data(){
        return{
            credits: [
                {
                    credTitle: "DC COMICS",
                    linkedElements: [
                        {
                            name: "Characters",
                            path: "/"
                        },
                        {
                            name: "Comics",
                            path: "/"
                        },
                        {
                            name: "Movies",
                            path: "/"
                        },
                        {
                            name: "TV",
                            path: "/"
                        },
                        {
                            name: "Games",
                            path: "/"
                        },
                        {
                            name: "Videos",
                            path: "/"
                        },
                        {
                            name: "News",
                            path: "/"
                        },
                    ]
                },
                {
                    credTitle: "DC",
                    linkedElements: [
                        {
                            name: "Terms Of Use",
                            path: "/",
                        },
                        {
                            name: "Privacy policy (New)",
                            path: "/",
                        },
                        {
                            name: "Ad Choices",
                            path: "/",
                        },
                        {
                            name: "Advertising",
                            path: "/",
                        },
                        {
                            name: "Jobs",
                            path: "/"
                        },
                        {
                            name: "Subscriptions",
                            path: "/",
                        },
                        {
                            name: "Talent Workshops",
                            path: "/",
                        },
                        {
                            name: "CPSC Certificates",
                            path: "/",
                        },
                        {
                            name: "Ratings",
                            path: "/",
                        },
                        {
                            name: "Shop Help",
                            path: "/",
                        },
                        {
                            name: "Contact Us",
                            path: "/",
                        },
                    ],
                },
                {
                    credTitle: "SITES",
                    linkedElements: [
                        {
                            name: "DC",
                            path: "/",
                        },
                        {
                            name: "MAD Magazine",
                            path: "/",
                        },
                        {
                            name: "DC Kids",
                            path: "/",
                        },
                        {
                            name: "DC Universe",
                            path: "/",
                        },
                        {
                            name: "DC Power visa",
                            path: "/",
                        },
                        
                    ],
                },
                {
                    credTitle: "SHOP",
                    linkedElements: [
                        {
                            name: "Shop DC",
                            path: "/",
                        },
                        {
                            name: "Shop DC Collectibles",
                            path: "/",
                        },
                    ]
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="maxi-container-foot">

            <div class="container d-flex">
                <div class="credits pt-4">
                    <div class="row align-items-start">
                        <div class="col-4 d-flex" v-for="singleCredit in credits">
                            <div class="box text-white">
                                <h5 class="foot-title pb-2">{{ singleCredit.credTitle }}</h5>
                                <ul class="credits-list">
                                    <li v-for="singleRef in singleCredit.linkedElements">
                                        <a href="#" class="text-link">{{singleRef.name}}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        
                    </div>
                </div>
                <div class="big-image text-white">
                    <img class="logo-foot" src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>

        <div class="last-foot-container p-5">
            <div class="container d-flex justify-content-between">
                <div class="button-cont">
                    <button class="btn btn-outline-primary">SIGN UP NOW!</button>
                </div>
                <div class="ref d-flex gap-3 align-items-center">
                    <div>
                        <a href="#" class="follow-title">FOLLOW US</a>
                    </div>
                    <div>
                        <img src="../assets/img/footer-facebook.png" alt="">
                    </div>
                    <div>
                        <img src="../assets/img/footer-twitter.png" alt="">
                    </div>
                    <div>
                        <img src="../assets/img/footer-youtube.png" alt="">
                    </div>
                    <div>
                        <img src="../assets/img/footer-pinterest.png" alt="">
                    </div>
                    <div>
                        <img src="../assets/img/footer-periscope.png" alt="">
                    </div>
                </div>
            </div>
        </div>


    </footer>
</template>

<style lang="scss" scope>
    @use "../styles/partials/variables";

    footer{
        background-color: variables.$color-secondary-light;
    };

    .maxi-container-foot{
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        padding-bottom: 2rem;
        padding-top: 1rem;
    }

    .credits{
        position: relative;
    }

    .credits-list{
        list-style: none;
        margin: 0;
        padding: 0;
    }

    .text-link{
        text-decoration: none;
        color: variables.$text-grey;
        font-size: .8rem;
    }

    .logo-foot{
        position: absolute;
        right: 20%;
        bottom: 10%;
        
    }
    
    .btn{
        border-radius: 0%;
        border: 2px solid variables.$color-primary;
        font-size: 1rem;
        color: white;
    }
    
    .follow-title{
        font-size: 1.2rem;
        text-decoration: none;
        color: variables.$color-primary;
        font-weight: 600;
    }

</style>