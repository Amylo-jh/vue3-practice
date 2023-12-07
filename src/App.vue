<template>
  <button @click="add">
    ADD
  </button>
  <h1>    {{ reversedMessage }}  </h1>
  <h1>    {{ msg.split('').reverse().join('') }}  </h1>
  <h1>    {{ msg.split('').reverse().join('') }}  </h1>
  <h1>    {{ msg.split('').reverse().join('') }}  </h1>
</template>

<script>
export default {
  data() {
    return {
      // Getter, Setter
      msg: 'Hello Computed!'
    }
  },
  methods: {
    // Setter
    add() {
      this.reverseddMessage += '!?'
    }
  },
  computed: {
    // Getter
    reversedMessage() {
      return this.msg.split('').reverse().join('')
    },
    // Getter, Setter
    reverseddMessage: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(newValue) {
        this.msg = newValue
      }
    }
  }
}
</script>