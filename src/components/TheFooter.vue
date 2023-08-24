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

            <div class="container d-flex justify-content-between">
                <div class="credits pt-5">
                    <div class="row align-items-start pb-4 pt-2">
                        <div class="col-4 d-flex" v-for="singleCredit in credits">
                            <div class="box text-white">
                                <h5 class="foot-title pb-2 fw-bold">{{ singleCredit.credTitle }}</h5>
                                <ul class="credits-list">
                                    <li v-for="singleRef in singleCredit.linkedElements">
                                        <a href="#" class="text-link">{{singleRef.name}}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        
                    </div>
                </div>
                <div class="big-image"></div>
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
                        <a href="https://www.facebook.com/dc/?locale=it_IT">
                            <img src="../assets/img/footer-facebook.png" alt="">
                        </a>
                    </div>
                    <div>
                        <a href="https://twitter.com/DCOfficial">
                            <img src="../assets/img/footer-twitter.png" alt="">
                        </a>
                    </div>
                    <div>
                        <a href="https://www.youtube.com/channel/UCiifkYAs_bq1pt_zbNAzYGg">
                            <img src="../assets/img/footer-youtube.png" alt="">
                        </a>
                    </div>
                    <div>
                        <a href="https://www.pinterest.it/dccomics/">
                            <img src="../assets/img/footer-pinterest.png" alt="">
                        </a>
                    </div>
                    <div>
                        <a href="https://www.pscp.tv/">
                            <img src="../assets/img/footer-periscope.png" alt="">
                        </a>
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

        .maxi-container-foot{
            background-image: url(../assets/img/footer-bg.jpg);
            background-size: cover;

            .container{

                .credits{
                    position: relative;
                    
                    .row{

                        .col-4{

                            .box{

                                .credits-list{
                                    list-style: none;
                                    margin: 0;
                                    padding: 0;

                                    li{
                                        
                                        .text-link{
                                            text-decoration: none;
                                            color: variables.$text-grey;
                                            font-size: .8rem;
                                        }
                                    }
                                }
                            }
                        }
                    }
                }

                .big-image{
                    background-image: url(../assets/img/dc-logo-bg.png);
                    width: 600px;
                    background-repeat: no-repeat;
                    background-position: center;
                    background-size: cover;
                }
            }

            .last-foot-container{
                
                .container{

                    .button-cont{

                        .btn{
                            border-radius: 0%;
                            border: 2px solid variables.$color-primary;
                            font-size: 1rem;
                            color: white;
                        }
                    }

                    .ref{

                        .follow-title{
                            font-size: 1.2rem;
                            text-decoration: none;
                            color: variables.$color-primary;
                            font-weight: 600;
                        }
                    }
                }
            }
        }
    };

    

    

    

   

   
    
    
    
    

</style>