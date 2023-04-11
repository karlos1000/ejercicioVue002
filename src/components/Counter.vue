<template>
    <div>
        <h1>{{ count }}</h1>
        <input type="number" v-model="count">
    </div>
    <div>
        <button v-on:click="increment">Aumentar</button>
        <button v-on:click="decrement">Disminuir</button>
    </div>
</template>

<script>
import { ref } from "vue";
export default {
    name: 'Counter',
    props: {
    },
    setup() {
        let count = ref(0);

        const increment = () => {
            count.value ++;
        }

        const decrement = () => {
            count.value --;
        }

        return {
            count,
            increment,
            decrement,
        }
    }
}
</script>

<style scoped></style>
