<script setup>
defineProps({
    title: {
      type: String,
      required: true,
    },
  });
</script>

<template>
  
  <div class="card">
    <h1>{{ title }}</h1>
    <slot>
        <p>Conteúdo padrão do card</p>
    </slot>
  </div>
  
</template>

<style scoped>
  .card {
    padding: 20px;
    border: 1px solid rgb(0, 0, 0);
    border-radius: 5px;
    box-shadow: 3px 3px 2px 2px gray;
  }
</style>