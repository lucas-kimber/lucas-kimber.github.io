<template>
    <div class="content-scroll-box">
        <Skills
            title="Languages"
            :skillarr="lang"
        />
        <Skills
            title="Tools"
            :skillarr="tools"/>
        <Skills
            title="Methodologies"
            :skillarr="methodologies"/>
        
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

const tools = ref([
    "Tauri",
    "Cargo",
    "Git",
    "Azure",
    "GitLab and Azure Pipelines",
    "Gherkin / Cypress / Cucumber",
    "Maven",
    "JUnit"
])

const methodologies = ref([
    "TDD",
    "BDD",
    "Scrum",
    "Agile",
    "Lean",
    "DevOps",
    "End-to-End Testing",
])

</script>