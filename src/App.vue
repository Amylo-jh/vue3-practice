<template>
  <h1>    {{ reversedMessage }}  </h1>
  <h1>    {{ msg.split('').reverse().join('') }}  </h1>
  <h1>    {{ msg.split('').reverse().join('') }}  </h1>
  <h1>    {{ msg.split('').reverse().join('') }}  </h1>
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello Computed!'
    }
  },
  methods: {
    reverseMessage() {
      return this.msg.split('').reverse().join('')
    }
  },
  computed: {
    reversedMessage() {
      return this.msg.split('').reverse().join('')
    }
  }
}
</script>