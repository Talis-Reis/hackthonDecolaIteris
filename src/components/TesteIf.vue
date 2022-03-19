<template>
    <div class="teste-if">
        <h1 v-if=podeVer>TALIS REIS</h1>
        <h1 v-else>MDS</h1>
    </div>    
</template>

<script>
export default {
    name: 'TesteIf',
    data(){
        return{
            podeVer: true
        }
    }
}
</script>

<style scoped>

</style>