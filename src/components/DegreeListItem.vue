<template>
    <li>
        <span>
            <span>{{ base }}</span>
            <sup>{{ exponent }}</sup>
        </span>
        <span class="equals">=</span>
        <span>{{ power }}</span>
    </li>
</template>

<style scoped>
    li {
        display: flex;
        align-items: center;
        text-align: left;
        border-bottom: 1px solid #E0E0E0;
        padding: 0.75rem;
    }
    .equals {
        margin: 0 0.5rem;
    }
</style>

<script>
export default {
  name: 'DegreeListItem',
  props: {
    base: {
      type: Number,
      default: 2,
    },
    exponent: {
      type: Number,
      default: 1,
      validator(value) {
        return value > -1
      }
    },
  },
  computed: {
    power() {
      return this.base ** this.exponent
    },
  },
}
</script>
