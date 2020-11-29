<template>
  <button class="base-button"
         :class="classes"
         :type="nativeType"
         v-on="$listeners">
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    variant: String,
    block: Boolean,
    nativeType: {
      type: String,
      default: 'button',
      validator: value => {
        return ['submit', 'button', 'reset'].indexOf(value) !== -1
      }
    },
  },

  computed: {
    classes() {
      return [
        this.variant ? 'base-button--' + this.variant : '',
        {
          'base-button--block': this.block
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .base-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    height: 50px;
    padding: 0 36px;
    background: transparent;
    text-align: center;
    white-space: nowrap;
    transition: .2s;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: 500;
    color: white;
    border: none;
    cursor: pointer;
    outline: none;

    &:hover,
    &:focus {
      opacity: .8;
    }

    &:active {
      opacity: .5;
    }

    &--primary {
      background-color: var(--primary-color);
    }

    &--accent {
      background-color: var(--accent-color);
    }

    &--block {
      width: 100%;
    }
  }
</style>
