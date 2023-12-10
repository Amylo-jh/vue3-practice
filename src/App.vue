<template>
  <h1
    :style="[fontStyle, backgroundStyle]"
    @click="changeStyle">
    Hello!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      fontStyle: {
        color: 'orange',
        fontSize: '20px'
      },
      backgroundStyle: {
        backgroundColor: 'black'
      }
    }
  },
  methods: {
    activate() {
      this.isActive = !this.isActive
    },
    changeStyle() {
      this.fontStyle.color = 'red',
      this.fontStyle.fontSize = '50px'
    }
  }
}
</script>

<style scoped>
  .active {
    color: red;
    font-weight: bold;
  }
</style>