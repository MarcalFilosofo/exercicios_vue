<template>
    <div :class="{'cliente' : !isPremimum, 'premium': isPremimum}">

        <div>Nome: {{ nome }}</div>
        <div>Número: {{ numero }}</div>
        <div>Email: {{ email }}</div>
        <div v-show="showIdade == true">Idade: {{ idade }}</div>
        <!-- <div v-else>Não informada</div> -->
        <!-- Segundos em um dia: {{ 60 * 60 * 24 }} -->
        <button @click="mudarCor">Mudar Cor</button>
    </div>
</template>

<script>
export default {
    data(){
        return{
            isPremimum: true,
        }
    },
    props: {
        nome: String,
        numero: String,
        email: String,
        idade: Number,
        showIdade: Boolean
    }, methods: {
        mudarCor(){
            this.isPremimum = !this.isPremimum;
        }
    }
}
</script>

<style scoped>
    .cliente {
        font-size: 1.5em;
        text-align: center;
        color: #999;
        margin-top: 50px;
    }

    .premium {
        font-size: 1.5em;
        text-align: center;
        color: #ffc508;
        margin-top: 50px;
    }
</style>