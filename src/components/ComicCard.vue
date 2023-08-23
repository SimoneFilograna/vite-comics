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
            <p class="card-text">{{name}}</p>
        </div>
    </div>
</template>