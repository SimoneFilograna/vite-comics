<script>
import TheHeader from "../src/components/TheHeader.vue";
import TheFooter from "../src/components/TheFooter.vue";
import BlueBar from "../src/components/BlueBar.vue";
import Comics from "../src/db/dc-comics.json";
import ComicCard from "../src/components/ComicCard.vue";

export default{
  components: {
    TheHeader,
    TheFooter,
    BlueBar,
    ComicCard,
  },

  data(){
    return{
      Comics,
    }
  }

}
</script>

<template>

  <body>
    <TheHeader></TheHeader>

    
    <main>
      <div class="jumbotron"></div>

      <div class="container">
        <div class="row">
          <div class="col-2" v-for="(singleComic, i) in Comics" :key="i">

            <ComicCard
             :img="singleComic.thumb"
             :name="singleComic.series" >
            </ComicCard>

          </div>
        </div>
      </div>

      <BlueBar></BlueBar>

    </main>

    <TheFooter></TheFooter>
  </body>

  

</template>

<style lang="scss">
  @use "../src/styles/partials/variables";
  @use "../src/styles/partials/mixins";

  body{
    background-color: variables.$color-secondary-light;
  }

  .jumbotron{
    background-image: url(./assets/img/jumbotron.jpg);
    height: 400px;
  }

  main{
    background-color: variables.$color-secondary-dark;

    .box{
      padding: 4rem 0;

      h2{
        color: white;
      }
    }
  }

</style>
