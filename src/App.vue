<template>
  <a
    href="https://naver.com"
    target="_blank"
    @click.prevent.once="handler">naver</a>

  <div
    class="parent"
    @wheel.passive="handlerA">
    <div
      class="child" />
  </div>
</template>

<script>
export default {
  methods: {
    handler() {

      console.log('ABC!')
    },
    handlerA(event) {
      console.log(event)
      console.log(event.target)
      console.log(event.currentTarget)
      console.log('A')
    },
    handlerB() {
      console.log('B')
    }
  }
}</script>

<style scoped lang="scss">
.parent {
  width: 200px;
  height: 100px;
  background-color: royalblue;
  margin: 10px;
  padding: 10px;
  overflow: auto;
  .child {
    width: 100px;
    height: 2000px;
    background-color: orange;
  }
}
</style>
