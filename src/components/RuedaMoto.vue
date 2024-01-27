<template>
    <h2>Ruedas</h2>
    <p>Marca: {{marca}}</p>
    <p>Color: {{color}}</p>
    <p>Material: {{material}}</p>
</template>
<script>
    export default {
        setup() {
            const marca = "GoodYear";
            const color = "grey";
            const material = "Plastico";
            return {
                marca,
                color,
                material
            }
        }
    }
</script>
<style>
</style>