<template>
    <main>

    <div class="container">
      <h1> &#8594; The content goes here &#8592;</h1>
    </div>
    
  </main>
</template>

<script>
  export default {
    name: 'MbMain'
  }
</script>

<style lang="scss" scoped>

  @import '../assets/style/mixins';
  @import '../assets/style/vars';

  main{
    background-color: black;
    color: $primary-color;
    padding: 50px 0;
  }

</style>