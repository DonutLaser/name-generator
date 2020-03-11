<template>
  <div id="app">
    <NamePreview :preview="name" />
    <div class="toolbar-row">
      <ButtonAny @click-event="addLetter" />
      <ButtonVowel @click-event="addLetter" />
      <ButtonConsonant @click-event="addLetter" />
      <ButtonSpace @click-event="addLetter" />
    </div>
    <div class="toolbar-row">
      <BaseCheckbox
        :name="'Capitalize first word'"
        @toggle="capitalizeFirstWord"
      />
    </div>
  </div>
</template>

<script>
import NamePreview from './components/NamePreview.vue'
import ButtonAny from './components/ButtonAny.vue'
import ButtonVowel from './components/ButtonVowel.vue'
import ButtonConsonant from './components/ButtonConsonant.vue'
import ButtonSpace from './components/ButtonSpace.vue'
import BaseCheckbox from './components/BaseCheckbox.vue'

export default {
  name: 'App',
  components: {
    NamePreview,
    ButtonAny,
    ButtonVowel,
    ButtonConsonant,
    ButtonSpace,
    BaseCheckbox
  },
  data: function () {
    return {
      name: '',
      capitalize: false

    }
  },
  methods: {
    addLetter: function (letter) {
      this.name += letter

      if (this.capitalize && this.name.length === 1) {
        this.name = this.name.toUpperCase()
      }
    },
    capitalizeFirstWord: function (capitalize) {
      this.capitalize = capitalize

      if (this.name) {
        if (this.capitalize) {
          this.name = this.name[0].toUpperCase() + this.name.slice(1)
        } else {
          this.name = this.name.toLowerCase()
        }
      }
    }
  }
}
</script>

<style>
.toolbar-row{
  width: fit-content;
  margin: 0 auto 10px auto;
}
</style>
