<script setup>
const props=defineProps(['firNumD','secNumD'])

</script>

<template>
       <input type="number" placeholder="Digite o primeiro número" @keyup="props.firNumD"/>
       <!-- <input type="number" placeholder="Digite o primeiro número" @keyup="firNumdigited"/> -->
      <input type="number" placeholder="Digite o segundo número" @keyup="props.secNumD"/>
      <!-- <input type="number" placeholder="Digite o segundo número" @keyup="secNumdigited"/> -->

</template>