<template>
    <div class="sidebar">
        <h2>Bienvenido</h2>
        <h3>Nombre {{ nombre }}</h3>
        <h3>Email {{ email }}</h3>
        <ul>
            <li><router-link to="/contador">Contador</router-link></li>
            <li><router-link to="/lista-de-tareas">Lista de Tareas</router-link></li>
            <li><router-link to="/registrar">Registrar</router-link></li>
        </ul>
    </div>
</template>

<script setup>
import { useRegistrarStore } from '@/modules/registro/stores/registrarStore';
import { ref, watch } from 'vue';
const registrarStore = useRegistrarStore()
const nombre = ref(registrarStore.nombre)
const email = ref(registrarStore.email)

/* watch supervisa la variable detectando los cambios, luego la funcion */
watch(() => registrarStore.nombre, (newValue) => {
    nombre.value = newValue;
});

watch(() => registrarStore.email, (newValue) => {
    email.value = newValue;
});
</script>

<style>
    .sidebar{
        width: 200px;
        padding: 20px;
    }
</style>