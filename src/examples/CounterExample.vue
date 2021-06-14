<template>
    <h2>Counter</h2>
    <div class="example">
        <div class="code">
            <pre v-highlightjs>
<code class="javascript">&lt;template>
    &lt;Counter :min="0" :init="1" :max="9" @valueUpdate="doSomething" />
&lt;/template>

&lt;script>
    import Counter from '../components/Counter'
    export default {
        name: 'Component Name',
        components: {
            Counter
        },
        methods: {
            doSomething(value) {
                alert('Value changed to: ' + value)
            }
        }
    }
&lt;/script>
</code>
            </pre>
        </div>
        <div class="component">
            <Counter />
            <Counter :min="0" :init="1" :max="9" @valueUpdate="valueChange" />
            <Counter :min="-3" :init="0" :max="3" />
        </div>
    </div>
    
</template>

<script>
import Counter from '../components/Counter'
export default {
    name: 'Counter Example',
    components: {
        Counter
    },
    methods: {
        valueChange(value) {
            alert('Value changed to: ' + value)
        }
    }
}
</script>
