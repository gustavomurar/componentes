<script setup>
import ExpandBox from './components/ExpandBox.vue';
import CardFull from './components/CardFull.vue';
const caixas = [
  { id: 1, title: 'Caixa 1', content: 'Conteúdo 1', qty: 100 },
  { id: 2, title: 'Caixa 2', qty: 30 },
  { id: 3, title: 'Caixa 3', content: 'Conteúdo 3' },
  { id: 4, title: 'Caixa 4' }
]
</script>

<template>
  <h1>Componentes</h1>
  <h2>Slots</h2>
  <Card title="Card 1">
    <h2>Meu subtítulo</h2>
    <p>Conteúdo do card 1</p>
  </Card>
  <card title="Card 2"></card>
  <CardFull>
    <h2>Meus dados</h2>
    <p>Body</p>
      <template #header>
        <h1>Meu Nome</h1>
      </template>
      <!--<template #footer>
        <p>Dados do card</p> 
      </template> -->
  </CardFull>
  <hr />
  <h2>Props</h2>
  <ExpandBox v-for="caixa in caixas" :key="caixa.id" v-bind="caixa" />
  <!-- <ExpandBox title="Caixa 1" content="Conteúdo secreto da caixa 1"/>
  <expand-box title="Caixa 2" qty="50"/>  -->
</template>

<style scoped></style>
