<template>
    <h1>Avion: </h1>
    <p>Modelo: {{ model}}</p>
    <p>Fabricante: {{ fabricante }}</p>
    <p>Color: {{ color[3] }}</p>
    <p>Precio: {{ price }}</p>
    <p v-if="power <= 500 && power >= 70">Potencia: {{ power }}</p>
    <p v-else>Potencia: <span style="color: red; font-weight: bold;">Valor Invalido</span></p>
    <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
    <RuedaAvion/>
    <button @click="upPower()">Aumentar Potencia</button>
    <button @click="downPower()">Bajar Potencia</button>

</template>
<script>
import { ref } from "vue";
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
        let power = ref(445);
        const upPower = ()=> {
            console.log("Aumentando potencia...");
            power.value = power.value + 1;
        }
        const downPower = () => {
            console.log("Disminuyendo potencia...");
            power.value = power.value - 1;
        }
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
            mensaje,
            upPower,
            downPower
        }
    }
}
</script>
<style></style>