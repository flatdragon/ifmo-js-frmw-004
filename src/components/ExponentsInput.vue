<template>
    <div class="input-group">
        <label>
            <input type="text" :value="value" @input="input">
        </label>
        <button title="Инкрементировать экспоненту" @click="increment">
            <plus-icon class="icon" />
        </button>
    </div>
</template>

<style>
    .input-group {
        display: flex;
        padding: 0.75rem;
    }
    label {
        display: flex;
        flex-grow: 1;
        margin-right: 0.75rem;
    }
    label > input {
        width: 100%;
    }
</style>

<script>
import PlusIcon from '../assets/plus-icon.svg'
const normalize = (value) => {
  value = value > 50 ? 50 : value
  value = value < 0 ? 0 : value
  return value
}
export default {
  name: 'ExponentsInput',
  components: { PlusIcon },
  props: {
    value: {
      type: Number,
      default: 0,
    },
  },
  methods: {
    input({ target }) {
      this.$emit('input', normalize(+target.value))
    },
    increment() {
      this.$emit('input', normalize(this.value + 1))
    },
  },
}
</script>