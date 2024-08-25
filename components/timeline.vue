<template>
    <div class="tl-item">
        <div class="tl-head">
            <h1>{{ pos }}</h1>
            <h2>{{ location }}, {{ start }} to {{ end }}</h2>
        </div>
        <p class="content"><slot /></p>
    </div>
</template>
<script setup>
    import { defineProps } from 'vue'
   const props = defineProps({
        pos: {
            type: String
        }, 
        location:{
            type: String
        }, 
        start:{
            type: String
        }, 
        end:{
            type: String
        }
    })
</script>
<style lang="scss" scoped>
.tl-item {
    font-family: "Poppins", sans-serif;
}
.tl-head {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
}
h1 {
    font-size: 24px;
    font-weight: 500;
}
h2 {
    font-size: 16px;
    font-weight: 300;
}
.content {
    flex-shrink: 0;
    padding-left: 20px;
}

@media screen and (max-width: 768px) {
    .tl-head {
        flex-direction: column;
    }
    h1 {
        font-size: 18px;
        font-weight: 500;
        margin-bottom: 0;
    }
    h2 {
        font-size: 14px;
        font-weight: 300;
        margin-bottom: 0;
        margin-top: 10px;
    }
    .content {
        padding-left: 0;
        font-size: 0.8em;
    }
}

@media screen and (max-width: 340px){
  
}

</style>