<template>
    <div class="newComponent">
        <h1>VUE JS</h1>
        <h2>{{first_name}}</h2>
    </div>
</template>

<script>

export default {
        name: 'newComponent',
        props: {
            first_name: String
        }
}
</script>

<style scoped>

</style>
