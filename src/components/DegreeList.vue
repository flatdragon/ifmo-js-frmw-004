<template>
    <div class="card">
        <div class="card-header">
            <div class="card-title">Степени</div>
        </div>
        <exponents-input v-model="exponents" />
        <ul>
            <degree-list-item
                v-for="exponent in exponents"
                :key="exponent"
                :base="2"
                :exponent="exponent"
            />
        </ul>
    </div>
</template>

<style scoped>
    .card {
        border: 1px solid #E0E0E0;
        border-radius: 4px;
        background: #FAFAFA;
        min-width: 300px;
        max-width: 100%;
    }
    .card-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid #E0E0E0;
        padding: 0.75rem;
    }
    .card-title {
        font-weight: bold;
        font-size: 1.15rem;
    }
    ul {
        padding: 0;
        margin: 0;
        list-style: none;
        border-top: 1px solid #E0E0E0;
    }
</style>

<script>
import DegreeListItem from './DegreeListItem'
import ExponentsInput from './ExponentsInput'
export default {
  name: 'DegreeList',
  components: { ExponentsInput, DegreeListItem },
  data: () => ({
    exponents: 3,
  }),
}
</script>