<template>
  <MyBtn>
    <template v-slot:text>banana</template>
    <template v-slot:icon>b</template>
  </MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
  components: {
    MyBtn
  }
}</script>