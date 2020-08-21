<template>
  <button class="c-button" :class="[`c-button--${color}`, style]">
      <template v-if="icon"><c-icon :name="icon" /></template>
      <template v-if="text">{{text}}</template>
  </button>
</template>

<script>
import cIcon from "@/components/c-icon.vue"

export default {
  name: "c-button",
  components: {
      cIcon
  },
  props: {
      icon: String,
      text: String,
      color: String,
      style: String,
  }
};
</script>

<style lang="scss" scoped>
.c-button {
    box-sizing: border-box;
    padding: 16px 16px;
    border: 0;
    border-radius: 4px;
    color: $c-light-100;
    fill: $c-light-100;
    background-color: $c-dark-900;
    cursor: pointer;

    svg {
        height: 16px;
    }

    @include modifier(deepPurple) {
        color: $c-dark-600;
        fill: $c-dark-600;
        background-color: $c-deepPurple-200;
    }
}
</style>