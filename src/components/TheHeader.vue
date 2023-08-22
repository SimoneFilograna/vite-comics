<script>
export default{
    data(){
        return{
            navItem: [
                {
                    name: "Character",
                    link: "/"
                },
                {
                    name: "Comics",
                    link: "/"
                },
                {
                    name: "Movies",
                    link: "/"
                },
                {
                    name: "TV",
                    link: "/"
                },
                {
                    name: "Games",
                    link: "/"
                },
                {
                    name: "Collectibles",
                    link: "/"
                },
                {
                    name: "Videos",
                    link: "/"
                },
                {
                    name: "Fans",
                    link: "/"
                },
                {
                    name: "News",
                    link: "/"
                },
                {
                    name: "Shop",
                    link: "/"
                },
                
            ]
        }
    }

}
</script>

<template>
    <div class="container">
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <div class="list-menu">
            <ul class="nav">
                <li class="nav-item" v-for="singleItem in navItem">
                    <a href="#" class="nav-link">{{singleItem.name}}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../styles/partials/variables";
    @use "../styles/partials/mixins";


    .container{
        @include mixins.center;
        padding: 2rem;
        justify-content: space-between;

        .logo{
            img{
                width: 80px;
            };
        };

        .list-menu{
            .nav{
                .nav-item {
                    .nav-link{
                        color: variables.$text-dark-grey;

                        &:hover {
                            color: variables.$color-primary;
                        };
                    };
                };
            }
        }

        

    }
</style>