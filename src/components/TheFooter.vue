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
        <div class="container">
            <div class="credits">
                <div class="raw">
                    <div class="col-4" v-for="singleCredit in credits">
                        <div class="box text-white">
                            <h4 class="foot-title">{{ singleCredit.credTitle }}</h4>
                            <ul>
                                <li v-for="singleRef in singleCredit.linkedElements">
                                    <a href="#"> {{singleRef.name}}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    
                </div>
            </div>
            <div class="big-image"></div>
        </div>
    </footer>
</template>

<style lang="scss" scope>
    @use "../styles/partials/variables";

    footer{
        background-image: url(../assets/img/footer-bg.jpg);
    }

</style>