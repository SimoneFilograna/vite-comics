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
                asdasjdasdas
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scope>
    @use "../styles/partials/variables";

    footer{
        background-image: url(../assets/img/footer-bg.jpg);
        padding-bottom: 2rem;
        padding-top: 1rem;
    };

    .credits-list{
        list-style: none;
        margin: 0;
        padding: 0;
    }

    .text-link{
        text-decoration: none;
        color: variables.$text-grey;
        font-size: .7rem;
    }
    

</style>