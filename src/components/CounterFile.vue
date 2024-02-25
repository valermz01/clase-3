<template>
    <div class="content-center">
    <img :src="require('../assets/img/Paisaje.jpg')" alt="Paisaje" style="width: 200px; height: auto;">
    <h1>{{ counter }}</h1>
    <button @click="incremento">increment</button>
    <button @click="reset" style="margin-top:10px;"> reset </button>
    </div>
</template>

<script>

    import { ref } from'vue';

    export default{
    setup() {
        const counter= ref(0);
        return{counter};
    },

    methods: {
        incremento(){
            this.counter++;
        },

        reset(){
            this.counter = 0;
        }
    }
    }
</script>

<style>

.content-center {
    display: flex;
    flex-direction: column;
    align-items: center; 
    justify-content: center;
    height: 220px;
    text-align: center;
}
</style>