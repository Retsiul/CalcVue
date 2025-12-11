<script setup>
const props = defineProps(['firNumD', 'secNumD'])

</script>

<template>
    <input type="number" placeholder="Digite o primeiro número" @keyup="props.firNumD" />
    <input type="number" placeholder="Digite o segundo número" @keyup="props.secNumD" />
</template>