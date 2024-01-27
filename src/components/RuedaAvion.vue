<template>
    <h2>Ruedas</h2>
    <p>Marca: {{marca}}</p>
    <p>Color: {{color}}</p>
    <p>Material: {{material}}</p>
</template>

<script>
export default {
    setup() {
        const marca = "MICHELIN";
        const color = "grey";
        const material = "pastico";
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