<template>
  <BaseButton
    :name="'Space'"
    @click-event="getSpace"
  />
</template>

<script>
import BaseButton from './BaseButton.vue'

export default {
  components: { BaseButton },
  methods: {
    getSpace: function () {
      this.$emit('click-event', ' ')
    }
  }
}
</script>
