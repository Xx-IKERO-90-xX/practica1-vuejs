<template>
    <h1>Coche</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Color: {{ color[1] }}</p>
    <p>Precio: {{ price }}</p>
    <p>Potencia: {{ power }}</p>
    <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
    <RuedaCoche />
</template>
<script>
import RuedaCoche from "./RuedaCoche.vue";
export default {
    components: {
        RuedaCoche
    },
    setup() {
        const brand = "Bentley";
        const model = "Bentayga";
        const color = ["Silver Frost", "Silver Storm", "Magnetic"];
        const price = 219819.00;
        const power = 449;
        const mensaje = {
            title: "sanpitopato",
            text: "citroen"
        };
        return {
            brand,
            model,
            color,
            price,
            power,
            mensaje
        }
    }
}
</script>
<style></style>