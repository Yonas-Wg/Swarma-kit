

<template>
        <div>
        <p>prop value is {{ prop1 }}</p>
        </div>
</template>

<script setup>
    defineProps({
        prop1: {
            type: String,
            required: true,
        }
    });
</script>

<style scoped>
div {
    background-color: #f0f0f0;
    padding: 20px;
    border-radius: 8px;
    }
</style>
