<template>
    <section>
        <h2>{{ title }}</h2>
        counter: {{$store.state.counter.counter}}
        <button v-on:click="$store.commit('counter/countUP')" class="add">+1</button>
        <button v-on:click="$store.commit('counter/reset')" class="reset">reset</button>
    </section>
</template>

<script>
export default {
    data: function() {
        return {
            title: 'Count App'
        }
    }
}
</script>

<style scoped>
section {
    padding: 30px;
}

h2 {
    color: #1e1e1e;
    font-weight: 600;
}

button {
    margin-top: 10px;
    color: #1e1e1e;
    border-radius: 20px;
    border: none;
    padding: 5px 10px;
}

.add {
    background: orange;
}

.reset {
    background: papayawhip;
}

button:hover {
    filter: brightness(105%);
}

</style>

