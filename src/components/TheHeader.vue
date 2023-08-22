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
    <div class="header-container">
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <div>
            <ul class="nav">
                <li class="nav-item" v-for="singleItem in navItem">
                    <a href="#" class="nav-link">{{singleItem.name}}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>