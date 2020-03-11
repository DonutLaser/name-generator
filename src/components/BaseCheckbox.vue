<template>
  <BaseButton
    :class="{ active: on }"
    :name="name"
    @click-event="onClick"
  />
</template>

<script>
import BaseButton from './BaseButton.vue'

export default {
  components: {
    BaseButton
  },
  props: {
    name: {
      type: String,
      default: 'Checkbox'
    }
  },
  data: function () {
    return {
      on: false
    }
  },
  methods: {
    onClick: function () {
      this.on = !this.on
      this.$emit('toggle', this.on)
    }
  }
}
</script>

<style>
.active {
  background-color: #aaaaaa77;
}
</style>
