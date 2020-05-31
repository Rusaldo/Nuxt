<template>
  <Modal :isOpen="isOpen" :title="title" @close="closeModal">
    <component :is="component" @close="closeModal" v-bind="props" />
  </Modal>
</template>

<script>
import ModalBus from '~/plugins/modalBus'
import Modal from './Modal.vue'

export default {
  components: {
    Modal
  },

  data() {
    return {
      isOpen: false,
      component: null,
      title: '',
      props: null
    }
  },

  created() {
    ModalBus.$on('open', ({ component, title = '', props = null }) => {
      this.component = component
      this.title = title
      this.props = props
      this.isOpen = true
    })

    if (process.client) {
      window.addEventListener('keyup', this.handleKeyup)
    }
  },

  beforeDestroy() {
    if (process.client) {
      window.removeEventListener('keyup', this.handleKeyup)
    }
  },

  methods: {
    closeModal() {
      this.isOpen = false
      // this.component = null
    },
    handleKeyup(e) {
      if (e.keyCode === 27) this.closeModal()
    }
  },
}
</script>
