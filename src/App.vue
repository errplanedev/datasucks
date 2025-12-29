<script setup lang="ts">
import { ref } from "vue";

const view = ref("hi");
</script>

<template>
    <nav>
        <button @click="view = 'import'">import .csv</button>
        <button @click="view = 'datasheets'">view datasheets</button>
    </nav>
    <main class="container">
        <div v-if="view == 'hi'">
            <h1>welcome</h1>
            <p>
                you can start by importing a csv file, or you can view your
                datasheets.
            </p>
        </div>
    </main>
</template>

<style scoped lang="css">
@import url("https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&display=swap");

body {
    font-family: "JetBrains Mono", monospace;
}

* {
    margin: 0;
    padding: 0;
    font-family: inherit;
}

nav {
    border-bottom: 1px solid lightslategray;
    padding: 0.15rem;
    display: flex;
    gap: 0.2rem;
}

button {
    border-radius: 0.15rem;
    border: 1px solid slategray;
    background-color: white;
    padding: 0.2rem 0.5rem;
    cursor: pointer;
}

button:hover {
    background-color: #f3f3f3;
}

button:active {
    background-color: #dadada;
}
</style>
