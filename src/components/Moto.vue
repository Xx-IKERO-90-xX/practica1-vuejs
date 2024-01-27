<template>
    <h1>Moto</h1>
    <p>Moto</p>
    <p>Modelo: {{ modelo }}</p>
    <p>Fabricante: {{ fabricante }}</p>
    <p>Color: {{ color[0] }}</p>
    <p>Precio: {{ precio }}</p>
    <p v-if="potencia >= 70 && potencia <= 500">Potencia: {{ potencia }}</p>
    <p v-else>Potencia: <span style="color: red; font-weight: bold;">Potencia Invalido</span></p>
    <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
    <RuedaMoto />
    <button @click="upPower()">Aumentar Potencia</button>
    <button @click="downPower()">Disminuir Potencia</button>
</template>
<script>
import {ref} from "vue";
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
        const potencia = ref(445);
        const upPower = ()=> {
            console.log("Aumentando potencia...");
            potencia.value = potencia.value + 1;   
        }
        const downPower = () => {
            console.log("Bajando potencia...");
            potencia.value = potencia.value - 1;
        }
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
            mensaje,
            upPower,
            downPower
        }
    }
}
</script>
<style></style>