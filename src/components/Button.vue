<template>
  <button @click="onClick()" :style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      default: "String",
    },
    color: {
      type: String,
      default: "green",
    },
  },
  methods: {
      onClick() {
          console.log('click')
      }
  }
};
</script>