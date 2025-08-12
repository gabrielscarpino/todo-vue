<script setup>
    const props = defineProps(['tarefasPendentes']);
</script>

<template>
    <header class="p-5 mb-4 mt-4 text-center bg-light rounded-3">
        <h1>Lista de tarefas</h1>
        <p v-if="props.tarefasPendentes > 0">
            Você possui {{ props.tarefasPendentes }} tarefas pendentes
        </p>
        <p v-else>Você não tem tarefas pendentes!</p>
    </header>
</template>