<template>
    <div class="counter" :class="hasError ? 'counter--error' : ''" >
        <button class="counter__sub" @click="substract">-</button>
        <input class="counter__value" type="tel" v-model="value">
        <button class="counter__add" @click="add">+</button>
    </div>
</template>

<script>
export default {
    name: 'Counter',
    props: ['init', 'min', 'max'],
    data() {
        return {
            value: 0,
            hasError: false,
        }
    },
    created() {
        if(this.init) {
            this.value = this.init
        }
    },
    methods: {
        substract() {
            if(this.min || this.min === 0) {
                if(this.value > this.min) {
                    this.value--
                } else {
                    this.handleError();
                }
            } else {
                this.value--
            }
        },
        add() {
            if(this.max) {
                if(this.value < this.max) {
                    this.value++
                } else {
                    this.handleError();
                }
            } else {
                this.value++
            }
        },
        handleError() {
            this.hasError = true;

            setTimeout(() => {
                this.hasError = false;
            }, 1000);
        }
    }
}
</script>