<template>
  <div id="app">
    <main>
      <v-reputations />
    </main>
  </div>
</template>

<script>
import vReputations from "@/views/v-reputations";

export default {
  name: "App",
  components: {
    vReputations,
  },
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
  min-height: calc(100vh - 56px);
  padding: 24px;
  margin: 0 auto 56px;

  @media #{$mq-lg} {
    max-width: 1024px;
    min-height: calc(100vh - 64px);
    padding: 64px 16px 64px;
    margin: 0 auto;
  }
}
</style>
