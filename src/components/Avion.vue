<template>
    <h1>Avion: </h1>
    <p>Modelo: {{ model}}</p>
    <p>Fabricante: {{ fabricante }}</p>
    <p>Color: {{ color[3] }}</p>
    <p>Precio: {{ price}}</p>
    <p>Potencia: {{ power }}</p>
    <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
    <RuedaAvion/>

</template>
<script>
import RuedaAvion from "./RuedaAvion.vue";
export default {
    components: {
        RuedaAvion
    },
    setup() {
        
        const model = "747-8i";
        const fabricante = "Boeing Commercial Planes";
        const color = ["red", "blue", "green", "orange", "yellow", "cyan", "white", "black", "grey", "pink", "purple"]
        const price = 393242.00;
        const power = 445;
        const mensaje = {
            title: "Boeing",
            text: "747"
        };
        return {
            model,
            fabricante,
            color,
            price,
            power,
            mensaje
        }
    }
}
</script>
<style></style>