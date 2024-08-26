<template>
    <div class="sk-item">
        <div class="sk-head">
            <h1>{{ title }}</h1>
        </div>
        <p class="content">
            <ul>
                <li v-for="sk in skillarr">{{ sk }}</li>
            </ul>
        </p>
    </div>
</template>
<script setup>
    import { defineProps } from 'vue'
   const props = defineProps({
        title: {
            type: String
        }, 
        skillarr:{
            type: Array
        }
    })
</script>
<style lang="scss" scoped>
.sk-item {
    font-family: "Poppins", sans-serif;
}
.sk-head {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
}
h1 {
    font-size: 16px;
    font-weight: 500;
    margin: 0;
}
.content {
    margin: 0;
    padding-left: 20px;
    padding-bottom: 20px;
    
    ul {
        list-style: none;
        display: flex;
        padding-left: 10px;
        margin: 0;
        flex-flow: wrap;
    
        & > li {
            margin-right: 10px;
            font-size: 1.4rem;
        }
    }
}




</style>