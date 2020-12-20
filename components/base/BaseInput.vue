<template>
  <div class="base-input">
    <input class="base-input__input"
           v-bind="$attrs"
           :value="value"
           @input="updateValue" >
  </div>
</template>

<script>
export default {
  inheritAttrs: false,

  props: {
    value: {
      type: [String, Number]
    }
  },

  methods: {
    updateValue(e) {
      this.$emit('input', e.target.value)
    }
  }
}
</script>

<style lang="scss" scoped>
  .base-input {
    width: 100%;

    &__input {
      -webkit-appearance: none;
      display: inline-flex;
      height: 50px;
      min-height: 50px;
      max-width: 100%;
      width: 100%;
      font-size: 16px;
      font-weight: 400;
      border-radius: 4px;
      border: 2px solid var(--border-color);
      font-family: var(--default-font-family);
      padding: 0 18px;
      transition: border-color .2s;
      outline: none;

      &:hover {
        border-color: var(--border-hover-color);
      }

      &:focus {
        border-color: var(--primary-color);
      }
    }
  }
</style>
