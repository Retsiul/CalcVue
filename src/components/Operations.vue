<script setup>
const props=defineProps(['value'])

</script>

<template>
    <select @change="props.value">
        <option value="">Selecione o operador</option>
        <option value="somar">+</option>
        <option value="subtrair">-</option>
        <option value="multiplicar">*</option>
        <option value="dividir">/</option>
    </select>
</template>