<script setup>
const props = defineProps(['operatString', 'result'])

</script>

<template>
    <div class="result-calc"> <span>{{ props.operatString }}</span> <span>{{ props.result }}</span> </div>
</template>