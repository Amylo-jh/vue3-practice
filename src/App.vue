<template>
  <MyBtn>Banana</MyBtn>
  <MyBtn :color="color"><span style="color: red">Banana</span></MyBtn>
  <MyBtn large color="royalblue">Cherry</MyBtn>
  <MyBtn>Banana</MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
  components: {
    MyBtn
  },
  data() {
    return {
      color: '#000'
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
