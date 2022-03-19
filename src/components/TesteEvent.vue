<template>
    <div class="teste-event">
        <p @click="verificaCaixaAlta">{{ mensagem }}</p>
    </div>
</template>

<script>
export default {
    name: 'TesteEvent',
    data(){
        return{
            mensagem: 'O rato roeu a roupa do rei de roma!'
        }
    },
    methods: {
        caixaAlta(){
            this.mensagem = this.mensagem.toUpperCase();
        },
        verificaCaixaAlta(){
            if(this.mensagem == this.mensagem.toUpperCase()){
                console.log("Mensagem em caixa alta");
                this.mensagem = this.mensagem.toLowerCase();
            }else{
                console.log("Mensagem normal");
                this.mensagem = this.mensagem.toUpperCase();
            }
        }
    },
}
</script>

<style scoped>

</style>