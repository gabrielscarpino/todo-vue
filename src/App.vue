<script setup>
import { reactive } from 'vue';

const estado = reactive({
    contador: 0,
})

function incrementar() {
    estado.contador++;
}

function decrementar() {
    estado.contador--;
}

const nomes = ['Gabriel', 'Laura', 'Paulo', 'Helena'];
</script>

<template>
    <h1>Calculadora VueJS</h1>

    {{ estado.contador }}

    <button @click="incrementar" type="button">+</button>
    <button @click="decrementar" type="button">-</button>
    <br>
    <ul>
        <li v-for="nome in nomes"> {{nome}} </li>
    </ul>
</template>

<style scoped></style>
