<template>
  <button @click="onClick">
    {{ name }}
  </button>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: 'Press Me'
    }
  },
  methods: {
    onClick: function () {
      this.$emit('click-event')
    }
  }
}
</script>

<style>
button {
  background-color: #00000000;
  border: 1px solid black;
  border-radius: 5px;
  min-height: 64px;
  min-width: 64px;
  font-size: 30px;
  padding: 10px;
  margin: 0 10px 0 10px;
}

button:hover {
  cursor: pointer;
  background-color: #cccccc77;
}

button:focus {
  outline: none;
}
</style>
