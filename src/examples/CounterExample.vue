<template>
    <h2>Counter</h2>
    <Counter :min="0" :init="1" :max="9" />
</template>

<script>
import Counter from '../components/Counter'
export default {
    name: 'Counter Example',
    components: {
        Counter
    }
}
</script>
