<template>
    <button @click="onClick()" :style="{ background:color }" class="btn">{{text}}</button>
</template>


<script>
    export default {
        name: "button-component",

        props:
        {
            text: String,
            color:String,
        },

        methods: {
            onClick() {
                console.log("Clicked!")
            }
        }
    }
</script>

