<template>
    <h1>Coche</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Color: {{ color[1] }}</p>
    <p>Precio: {{ price }}</p>
    <p v-if="power <= 500 && power >= 70">Potencia: {{ power }}</p>
    <p v-else>Potencia: <span style="color: red; font-weight: bold;">Valor Invalido</span></p>
    <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
    <RuedaCoche />
    <button @click="upPower()">Aumentar Potencia</button>
    <button @click="downPower()">Bajando Potencia</button>
</template>
<script>
import RuedaCoche from "./RuedaCoche.vue";
import { ref } from "vue";
export default {
    components: {
        RuedaCoche
    },
    setup() {
        const brand = "Bentley";
        const model = "Bentayga";
        const color = ["Silver Frost", "Silver Storm", "Magnetic"];
        const price = 219819.00;
        let power = ref(442);
        const upPower = () => {
            console.log("Aumentando precio...");
            power.value = power.value + 1;
        };
        const downPower = () => {
            console.log("Bajando precio...");
            power.value = power.value - 1;
        };
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
            mensaje,
            upPower,
            downPower
        }
    }
}
</script>
<style></style>