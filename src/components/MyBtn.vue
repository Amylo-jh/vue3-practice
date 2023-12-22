<template>
  <div class="btn">
    <slot />
  </div>
  <h1 @click="$emit('click')">
    ABC
  </h1>
  <input
    type="text"
    v-model="msg">
</template>

<script>
export default {
    emits: [
        'changeMsg',
        'click'
    ],
    data() {
        return {
            msg: ''
        }
    },
    watch: {
        msg() {
            this.$emit('changeMsg')
        }
    }
}</script>

<style scoped>
    .btn {
        display: inline-block;
        margin : 4px;
        padding: 6px 12px;
        border-radius: 4px;
        background-color: gray;
        color: white;
        cursor: pointer;
    }
</style>