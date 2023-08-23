<script>
export default {
    props: {
        img: String,
        name: String,
    }
}
</script>

<template>
    <div class="card">
        <img :src="img" class="card-img-top" alt="">
        <div class="card-body">
            <p class="card-text">{{name.toUpperCase()}}</p>
        </div>
    </div>
</template>

<style lang="scss" scope>

    .card{
        background-color: transparent;

        .card-img-top{
            object-fit: cover;
            object-position: top;
            aspect-ratio: 1/1;
    }
        .card-body{
            padding: 1rem 0;
            color: white;
        }
    }

    
</style>

