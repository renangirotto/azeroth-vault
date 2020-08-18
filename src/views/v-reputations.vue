<template>
  <div id="vReputations" class="v-reputations">
    <h1 class="t-page">Reputations</h1>
    <p>Your current progression with all factions beeing exalted is <strong class="t-highlight"><span>12/100</span></strong>.</p>
    <div class="v-reputations__grid">
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
      <div class="v-reputations__grid__item">
        <c-reputation />
      </div>
    </div>
  </div>
</template>

<script>
import cReputation from '@/components/reputation/c-reputation.vue'

export default {
    name: 'v-reputations',
    components: {
      cReputation
    }
}
</script>

<style lang="scss" scoped>
  .v-reputations {

    // grid to display expansions reputation list
    @include element(grid) {
      display: grid;
      grid-template-columns: 1fr;
      grid-template-rows: 1fr;
      grid-column-gap: 32px;
      grid-row-gap: 56px;

      @media #{$mq-sm} {
        grid-template-columns: 1fr 1fr;
      }

      @media #{$mq-lg} {
        grid-template-columns: 1fr 1fr 1fr;
      }

      @media #{$mq-xl} {
        grid-template-columns: 1fr 1fr 1fr 1fr;
      }

      // grid child
      @include element(item) {
        
      }
    }
  }
</style>