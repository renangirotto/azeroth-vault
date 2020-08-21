<template>
  <div class="c-textField">
      <input :type="fieldType" :placeholder="placeholder" />
  </div>
</template>

<script>
export default {
    name: 'c-text-field',
    props: {
        fieldType: {
            type: String,
            required: true
        },
        placeholder: {
            type: String,
            required: true
        },
    }
}
</script>

<style lang="scss" scoped>
.c-textField {
    input {
        box-sizing: border-box;
        width: 100%;
        padding: 16px;
        border: 0;
        border-bottom: 2px solid $c-dark-900;
        border-radius: 4px 4px 0 0;
        color: $c-light-100;
        background-color: $c-dark-600;
        transition: border-color .25s ease-in-out;

        &:focus {
            border-bottom: 2px solid $c-deepPurple-200;
        }
    }
}
</style>