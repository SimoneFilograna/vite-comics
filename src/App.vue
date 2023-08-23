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

      <div class="container pt-5 position-relative">

        <div>
          <a class="btn btn-primary current-button" href="#" role="button">CURRENT SERIES</a>
        </div>

        <div class="row g-4">
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
  }

  .current-button{
    background-color: variables.$color-primary;
    font-size: 1.5rem;
    position: absolute;
    top: -20px;
    left: -10px;
  }

</style>
