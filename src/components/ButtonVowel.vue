<template>
  <BaseButton
    :name="'Vowel'"
    @click-event="generateRandomVowel"
  />
</template>

<script>
import BaseButton from './BaseButton.vue'

export default {
  components: { BaseButton },
  methods: {
    generateRandomVowel: function () {
      const letters = ['a', 'e', 'i', 'o', 'u']
      const index = Math.floor(Math.random() * letters.length)

      this.$emit('click-event', letters[index])
    }
  }
}
</script>
