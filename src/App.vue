<template>
  <header>
    <img alt="Vue logo" src="./assets/img/logo.png">
    <h1>Vue utilities</h1>
  </header>
  <main>
    <CounterExample />
  </main>
</template>

<script>
import CounterExample from './examples/CounterExample';

export default {
  name: 'App',
  components: {
    CounterExample
  }
}
</script>