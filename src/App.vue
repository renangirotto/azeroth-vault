<template>
  <div id="app">
    <main>
      <v-search />
    </main>
  </div>
</template>

<script>
import vSearch from "@/views/v-search";

export default {
  name: "App",
  components: {
    vSearch,
  }
};
</script>

<style lang="scss">
html,
body {
  background-color: $c-dark-800;

  // Change text select
  ::-moz-selection {
    /* Code for Firefox */
    background-color: $c-deepPurple-200;
    color: $c-light-100;
  }
  // Change text select
  ::selection {
    background-color: $c-deepPurple-200;
    color: $c-light-100;
  }
}

main {
  box-sizing: border-box;
  max-width: 768px;
  min-height: 100vh;
  padding: 48px 24px;
  margin: 0 auto;

  @media #{$mq-md} {
    padding: 64px 16px;
  }

  @media #{$mq-lg} {
    max-width: 1200px;
    margin: 0 auto;
  }
}
</style>
