<template>
  <div id="vSearch" class="v-search">
    <h1 class="t-hero">Azeroth Vault</h1>
    <p>See through your character progression!</p>
    <div class="v-search__box">
        <c-textField fieldType="text" placeholder="Character name" />
        <span></span>
        <c-textField fieldType="text" placeholder="Realm name" />
        <c-button icon="arrow-right" color="deepPurple" />
    </div>
  </div>
</template>

<script>
import cTextField from '@/components/c-textField.vue'
import cButton from "@/components/c-button.vue"

export default {
  name: "v-search",
  components: {
    cTextField,
    cButton
  }
};
</script>

<style lang="scss" scoped>
.v-search {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: calc(100vh - 96px);
  margin: 0 auto;

  @media #{$mq-md} {
    min-height: calc(100vh - 128px);
  }

  @include element(box) {
    display: grid;
    grid-template-columns: 1fr;
    grid-row-gap: 16px;
    width: 100%;
    max-width: 360px;

    @media #{$mq-sm} {
      grid-template-columns: 40% auto 40% 10%;
      grid-column-gap: 16px;
      max-width: 600px;
    }
  }

  p {
    text-align: center;
  }

  // Divider of textFields
  span {
    display: none;
    justify-content: center;
    align-items: center;

    @media #{$mq-sm} {
      display: flex;
    }

    &::after {
      content: '-';
    }
  }
}
</style>