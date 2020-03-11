<template>
  <button
    class="btn"
    @click="onClick"
  >
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
.btn {
  background-color: #00000000;
  border: 1px solid black;
  border-radius: 5px;
  height: 64px;
  min-width: 64px;
  font-size: 30px;
  padding: 10px;
  margin: 0 10px 0 10px;
}

.btn:hover {
  cursor: pointer;
  background-color: #cccccc77;
}

.btn:active {
  background-color: #aaaaaa77;
}

.btn:focus {
  outline: none;
}
</style>
