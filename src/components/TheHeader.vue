<script>
export default{
    data(){
        return{
            navItem: [
                {
                    name: "CHARACTERS",
                    link: "/"
                },
                {
                    name: "COMICS",
                    link: "/"
                },
                {
                    name: "MOVIES",
                    link: "/"
                },
                {
                    name: "TV",
                    link: "/"
                },
                {
                    name: "GAMES",
                    link: "/"
                },
                {
                    name: "COLLECTIBLES",
                    link: "/"
                },
                {
                    name: "VIDEOS",
                    link: "/"
                },
                {
                    name: "FANS",
                    link: "/"
                },
                {
                    name: "NEWS",
                    link: "/"
                },
                {
                    name: "SHOP",
                    link: "/"
                },
                
            ]
        }
    }

}
</script>

<template>
    <header>
        <div class="container">

            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>

            <div class="list-menu">
                <ul class="nav">
                    <li class="nav-item" v-for="singleItem in navItem">
                        <a href="#" class="nav-link p-3">{{singleItem.name}}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use "../styles/partials/variables";
    @use "../styles/partials/mixins";

    header{
        background-color: white
    }
    .container{
        @include mixins.center;
        padding: 1rem;
        justify-content: space-between;
    }

    .logo{
        img{
            width: 80px;
        };
    };
    
    .nav-link{
        color: variables.$text-dark-grey;

    &:hover {
        color: variables.$color-primary;
        };

    &:focus {
        color: variables.$color-primary;
        };

    };
    
    .nav-item{
        font-size: .8rem;
        font-weight: 700;
    };
            
        

</style>