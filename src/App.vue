<template>
  <button @click="handler">
    Click Me!
  </button>
  <ul>
    <li
      v-for="{id, name} in newFruits"
      :key="id">
      {{ name }} - {{ id }}
    </li>
    {{ newFruits }}
  </ul>
</template>

<script>
import shortid from 'shortid'

export default {
  data() {
    return {
      fruits: ['Apple', 'Banana', 'Cherry']
    }
  },
  computed: {
    newFruits() {
      return this.fruits.map( fruit => ({
          id: shortid.generate(),
          name: fruit
      }))
    }
  },
  methods: {
    handler() {
      this.fruits.push('Orange')
    }
  }
}
</script>