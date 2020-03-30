<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div>
      <a class="task-link" target="_blank" href="https://kodaktor.ru/frmw_004">Задание FRMW-004</a>
    </div>
    <degree-list />
    <div class="author">Автор: <strong>Кочетыгов Андрей</strong></div>
  </div>
</template>

<script>
import DegreeList from './components/DegreeList'
export default {
  name: 'App',
  components: { DegreeList },
}
</script>

<style>
  body {
    margin: 0;
    background: #ebeced;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    min-height: 100vh;
    padding-bottom: 3rem;
    padding-top: 3rem;
  }

  input {
    border-radius: 4px;
    border: 1px solid #eee;
    padding: 0.5rem 0.75rem;
    outline: none;
  }

  button {
    border-radius: 4px;
    border: 0;
    padding: 0.5rem 0.75rem;
    outline: none;
    color: #fff;
    background: #2c3e50;
    cursor: pointer;
  }

  input:focus {
    border-color: #4CAF50;
    box-shadow: 0 0 8px #4CAF50;
  }

  .author {
    margin-top: 0.75rem;
  }

  .task-link {
    display: inline-block;
    margin-bottom: 0.75rem;
  }

  .icon {
    display: block;
    height: 1em;
    width: 1em;
    fill: currentColor;
  }
</style>
