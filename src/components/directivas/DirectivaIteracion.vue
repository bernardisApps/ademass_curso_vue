<template>
    <div class="container">
        <div class="row mx-auto">
            <div class="col-md-6 mx-auto">
                <ul class="list-group">
                    <li class="list-group-item list-group-item-action" v-for="(nombre, index) in nombres" :key="index">{{ nombre }}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
let nombres = ref(['matias', 'bruno', 'florencia']);
</script>

<style scoped></style>