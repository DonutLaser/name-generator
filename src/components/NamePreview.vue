<template>
  <div id="name-preview">
    <h1
      v-if="!preview"
      id="placeholder"
    >
      {{ placeholder }}
    </h1>
    <h1 id="preview">
      {{ preview }}
    </h1>
  </div>
</template>

<script>
export default {
  props: {
    preview: {
      type: String,
      default: ''
    }
  },
  data: function () {
    return {
      placeholder: 'Choose between consonants and vowels to generate a name'
    }
  }
}
</script>

<style>
#name-preview {
  width: 100%;
  height: 40vh;
}

#preview, #placeholder {
  position: relative;
  margin-left: auto;
  margin-right: auto;
  width: fit-content;
  top: 50%;
  transform: translateY(-50%);
  font-family: Arial;
}

#preview {
  font-size: 80px;
}

#placeholder {
  font-style: italic;
  color: #77777777;
}
</style>
