<template>
  <BaseButton
    :name="'Consonant'"
    @click-event="generateRandomConsonant"
  />
</template>

<script>
import BaseButton from './BaseButton.vue'

export default {
  components: { BaseButton },
  methods: {
    generateRandomConsonant: function () {
      const letters = [
        'b', 'c', 'd', 'f', 'g',
        'h', 'j', 'k', 'l', 'm',
        'n', 'p', 'q', 'r', 's',
        't', 'v', 'w', 'x', 'y',
        'z'
      ]
      const index = Math.floor(Math.random() * letters.length)

      this.$emit('click-event', letters[index])
    }
  }
}
</script>
