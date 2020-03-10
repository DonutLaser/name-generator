<template>
  <BaseButton
    :name="'Any letter'"
    @click-event="generateRandomLetter"
  />
</template>

<script>
import BaseButton from './BaseButton.vue'

export default {
  components: { BaseButton },
  methods: {
    generateRandomLetter: function () {
      const letters = [
        'a', 'b', 'c', 'd', 'e',
        'f', 'g', 'h', 'i', 'j',
        'k', 'l', 'm', 'n', 'o',
        'p', 'q', 'r', 's', 't',
        'u', 'v', 'w', 'x', 'y',
        'z'
      ]

      const index = Math.floor(Math.random() * letters.length)

      this.$emit('click-event', letters[index])
    }
  }
}
</script>
