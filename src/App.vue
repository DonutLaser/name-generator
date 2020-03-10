<template>
  <div id="app">
    <NamePreview :preview="name" />
    <div id="toolbar">
      <ButtonAny @click-event="addLetter" />
      <ButtonVowel @click-event="addLetter" />
      <ButtonConsonant @click-event="addLetter" />
    </div>
  </div>
</template>

<script>
import NamePreview from './components/NamePreview.vue'
import ButtonAny from './components/ButtonAny.vue'
import ButtonVowel from './components/ButtonVowel.vue'
import ButtonConsonant from './components/ButtonConsonant.vue'

export default {
  name: 'App',
  components: {
    NamePreview,
    ButtonAny,
    ButtonVowel,
    ButtonConsonant
  },
  data: function () {
    return {
      name: ''
    }
  },
  methods: {
    addLetter: function (letter) {
      this.name += letter
    }
  }
}
</script>

<style>
#toolbar {
  width: fit-content;
  margin-left: auto;
  margin-right: auto;
}
</style>
