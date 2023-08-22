<script>
import TheHeader from "../src/components/TheHeader.vue";
import TheFooter from "../src/components/TheFooter.vue";

export default{
  components: {
    TheHeader,
    TheFooter

  }
}
</script>

<template>

  <TheHeader></TheHeader>

  <main>
    <div class="container">
      <div class="box">
        <h2>Content goes here</h2>
      </div>
    </div>
  </main>

  <TheFooter></TheFooter>

</template>

<style lang="scss">
  @use "../src/styles/partials/variables";
  @use "../src/styles/partials/mixins";

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
