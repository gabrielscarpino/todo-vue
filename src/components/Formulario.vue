<script setup>
const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp']);
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row responsivo_geral">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required type="text"
                    placeholder="Digite a tarefa" class="form-control responsivo_geral">
            </div>
            <div class="col-md-2 text-center  responsivo_botao ">
                <button type="submit" class="btn btn-primary ">Cadastrar</button>
            </div>
            <div class="col-md-12 col-lg-2">
                <select @change="props.trocarFiltro" class="form-control responsivo_select text-center">
                    <option value="todas">Todas as tarefas</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>

<style scoped>

select:hover {
    cursor: pointer;
}

@media (max-width: 767px) {

    .responsivo_geral {
        display: block;
        text-align: center;
    }

    .responsivo_select {
        margin: 0 auto;
    }

    .responsivo_botao {
        margin: 24px auto;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {

    .responsivo_geral {
        display: block;
        text-align: center;
    }

    .responsivo_select {
        margin: 0 auto;
        
    }

    .responsivo_botao {
        margin: 24px auto;
    }

}
</style>
