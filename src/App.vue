<template>
  <MyBtn @click="log" @change-msg="LogMsg">
    Banana
  </MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
  components: {
    MyBtn
  },
  methods: {
    log() {
      console.log('Click!')
    },
    LogMsg(msg) {
      console.log(msg)
    }
  }
}
</script>