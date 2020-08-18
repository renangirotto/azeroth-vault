<template>
  <div class="c-accordion">
    <h4 class="c-accordion__title" @click="open = !open">
      {{title}}
      <template v-if="!open">
          <c-icon name="plus" />
      </template>
      <template v-else-if="open">
          <c-icon name="minus" />
      </template>
    </h4>
    <div class="c-accordion__container" v-if="open">
      <slot name="container"></slot>
    </div>
  </div>
</template>

<script>
import cIcon from "@/components/c-icon.vue";

export default {
  name: "c-accordion",
  components: {
    cIcon,
  },
  props: {
    title: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      open: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.c-accordion {
  // tooltip for collapse
  @include element(title) {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-weight: 700;
    font-size: 22px;
    cursor: pointer;

    svg {
      width: 22px;
      height: 22px;
      fill: $c-light-100;
    }
  }

  @include element(container) {
    margin-top: 12px;
  }
}
</style>