<template>
    <div class="contador">
        <div class="valor-contador">{{valor}}</div>
        <div class="botoes">
            <div @click="increment" class="botao-contador">+</div>
            <div @click="decrement" class="botao-contador">-</div>
        </div>
    </div>    
</template>

<script>
export default {
    name: 'newContador',
    data(){
        let valor = 0
        return{
            valor
        }
    },
    methods:{
        increment(){
            this.valor += 1
        },
        decrement(){
            if(this.valor <= 0){
                alert("Valor já chegou no zero!")
            }else{
                this.valor -= 1
            }
        }
    }
}
</script>

<style scoped>
    .botoes{
        display: flex;
        justify-content: center;
        align-content: center;
    }
    .botao-contador{
        width: 50px;
        height: 50px;
        background-color: tomato;
        border: 1px solid black;
        margin-right: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .valor-contador{
        padding: 20px;
        font-size: 50px;
    }
</style>