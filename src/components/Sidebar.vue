<template>
    <div class="sidebar">
        <h2>Barra Lateral</h2>
        <ul>
            <li><router-link to="/contador">Contador</router-link></li>
            <li><router-link to="/lista-de-tareas">Lista de Tareas</router-link></li>
            <li><router-link to="/registrar">Registrar</router-link></li>
        </ul>
    </div>
</template>

<script setup>

</script>

<style>
    .h2{
        color: black;
    }
    .sidebar{
        width: 200px;
        background-color: antiquewhite;
        padding: 20px;
    }
</style>