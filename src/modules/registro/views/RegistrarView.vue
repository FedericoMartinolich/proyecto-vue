<template>
    <div>
        <h2>Formulario de Registro</h2>
        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre:</label>
                <Field type="text" name="nombre" placeholder="ingrese su nombre"/>
                <ErrorMessage name="nombre"></ErrorMessage>
            </div>
            <div class="form">
                <label for="correo">Correo:</label>
                <Field type="email" name="email" placeholder="ingrese su email"/>
                <ErrorMessage name="email"></ErrorMessage>
            </div>
            <div class="form">
                <label for="nombre">Nombre:</label>
            <button type="submit">Registrar</button>
            </div>            
        </Form>
    </div>
</template>

<script setup>
    import {Form, Field, ErrorMessage} from 'vee-validate'
    import {schema} from '../schemas/validationSchema'

    const onSubmit = () => {
        console.log('Se ha enviado el form correctamente');
    }
</script>

<style scoped>
    .form{
        margin-bottom: 10px;
    }
</style>