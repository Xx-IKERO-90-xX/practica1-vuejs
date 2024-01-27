<template>
    <h1>Moto</h1>
    <p>Moto</p>
    <p>Modelo: {{ modelo }}</p>
    <p>Fabricante: {{ fabricante }}</p>
    <p>Color: {{ color[0] }}</p>
    <p>Precio: {{ precio }}</p>
    <p>Potencia: {{ potencia }}</p>
    <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
    <RuedaMoto />
</template>
<script>
import RuedaMoto from "./RuedaMoto.vue"
export default {
    components: {
        RuedaMoto
    },
    setup() {
        const modelo = "CBR1000RR-R Fireblade";
        const fabricante = "HONDA";
        const color = ["red", "blue", "green", "orange", "yellow", "cyan", "white", "black", "grey", "pink", "purple"];
        const precio = 20900.00;
        const potencia = 445;
        const mensaje = {
            title: "Moto Fireblade",
            text: "CBR1000RR-R"
        };
        return {
            modelo,
            fabricante,
            color,
            precio,
            potencia,
            mensaje
        }
    }
}
</script>
<style></style>