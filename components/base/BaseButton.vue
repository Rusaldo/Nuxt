<template>
  <button class="base-button"
         :class="classObject"
         :type="nativeType"
         v-on="$listeners">
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    type: String,
    nativeType: {
      type: String,
      default: 'button',
      validator: value => {
        return ['submit', 'button', 'reset'].indexOf(value) !== -1
      }
    },
    expanded: Boolean,
    outlined: Boolean
  },

  computed: {
    classObject() {
      return {
        'base-button--primary': this.type === 'primary',
        'base-button--outlined': this.outlined,
        'base-button--expanded': this.expanded

      }
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
    padding: 0 18px;
    background: transparent;
    border: none;
    border-radius: 4px;
    text-align: center;
    white-space: nowrap;
    transition: .2s;
    font-size: 16px;
    border: 2px solid var(--border-color);
    cursor: pointer;

    &:hover {
      border-color: var(--border-hover-color);
    }

    &--primary {
      background: var(--primary-color);
      color: var(--text-white-color);
      border-color: transparent;

      &:hover {
        background: var(--primary-light-color);
        border-color: transparent;
      }
    }

    &--primary.base-button--outlined {
      background: transparent;
      border-color: var(--primary-color);
      color: var(--primary-color);

      &:hover {
        background: var(--primary-color);
        color: var(--text-white-color);
      }
    }

    &

    &--expanded {
      width: 100%;
    }
  }
</style>
