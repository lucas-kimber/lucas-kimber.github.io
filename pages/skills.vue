<template>
    <div>
        <Skills
            title="Languages"
            :skillarr="lang"
        />
    </div>
</template>
<script setup>
import { ref } from 'vue'

const lang = ref([
    "Rust",
    "Java",
    "Python",
    "Typescript",
    "SQL",
    "C#",
])

</script>