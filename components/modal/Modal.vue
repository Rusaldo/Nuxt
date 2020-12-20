<template>
  <transition name="fade">
    <div class="modal-backdrop"
      v-show="isOpen"
      :class="{open: isOpen}"
      @click="$emit('close')">

      <div class="modal-dialog" :class="{ open: isOpen }" @click.stop>
        <button class="modal-close" @click="$emit('close')">&#x2715;</button>
        <div class="modal-title" v-if="title">{{ title }}</div>
        <div class="modal-body">
          <slot />
        </div>
      </div>

    </div>
  </transition>
</template>

<script>
export default {
  props: {
    isOpen: Boolean,
    title: String
  }
}
</script>

<style lang="scss" scoped>
  .modal-backdrop {
    background: rgba(0, 0, 0, 0.7);
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 18px;
    z-index: 100;
  }

  .modal-dialog {
    width: 480px;
    background: rgb(255, 255, 255);
    padding: 18px;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
    border-radius: 0.3rem;
    transition: transform 0.3s;
    position: relative;
  }

  .modal-title {
    font-size: 24px;
    text-align: center;
    margin-bottom: 18px;
    color: var(--primary-color);
    border-bottom: 1px solid var(--border-color);
    padding-bottom: 18px;
  }

  .modal-body {
    font-size: 18px;
    padding-bottom: 18px;
  }

  .modal-close {
    position: absolute;
    top: 12px;
    right: 12px;
    font-size: 20px;
    color: var(--text-dark-color);
    background: transparent;
    border: none;
    z-index: 2;
    cursor: pointer;
    width: 32px;
    height: 32px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0;

    &:hover {
      color: gray;
    }
  }
</style>
