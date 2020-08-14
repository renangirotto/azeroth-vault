<template>
  <div id="app">
    <c-navbar/>
    <main>
      <v-read-list />
    </main>
  </div>
</template>

<script>
import cNavbar from '@/components/c-navbar.vue'
import vReadList from '@/views/v-readList'

export default {
  name: 'App',
  components: {
    cNavbar,
    vReadList
  }
}
</script>

<style lang="scss">
html, body {
  background-color: $c-dark-900;
}

main {
  box-sizing: border-box;
  max-width: 768px;
  min-height: calc(100vh - 56px);
  padding: 24px;
  margin: 0 auto;

  @media #{$mq-lg} {
    max-width: 1024px;
    min-height: calc(100vh - 64px);
    padding: 64px 16px 64px;
    margin: 0 auto;
  }
}
</style>
