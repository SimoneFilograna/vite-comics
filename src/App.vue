<script>
import TheHeader from "../src/components/TheHeader.vue";
import TheFooter from "../src/components/TheFooter.vue";
import BlueBar from "../src/components/BlueBar.vue"

export default{
  components: {
    TheHeader,
    TheFooter,
    BlueBar,

  }
}
</script>

<template>

  <body>
    <TheHeader></TheHeader>

    <main>
      <div class="container">
        <div class="box">
          <h2>Content goes here</h2>
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
