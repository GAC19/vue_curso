<template>
    <div>
        <h1>coche</h1>
        <p>marca: {{brand}}</p>
        <p>modelo: {{model}}</p>
        <p>color: 
            <span v-for="(color, index) in colors" :key="index">
            {{index}}:
            {{color}} -
            </span>
        </p>

        <p>color2:
            <ul>
                <li v-for="(color, index) in colors" :key="index">
                {{index}}:{{color}}
                </li>
            </ul>

        </p> 
        <p>precio : {{price}}</p>
        {{mensaje.title}} - {{mensaje.texto}}
    </div>
</template>

<script>

export default {
    // data() {
    //     return {
    //         brand:"Audi",
    //         model:"A4",
    //         color:"azul",
    //         price:38000
    //     }
    // },

    setup() {
        const brand="Audi";
        const modelo="A5";
        const colors=["azul", "morado", "rojo", "amarillo"];
        const price=45000;
        const mensaje={
            title:"estoy bien",
            texto:"welcome"};
    
    return{
        brand,
        modelo,
        colors,
        price,
        mensaje,
    };
}

};
</script>

<style>
</style>