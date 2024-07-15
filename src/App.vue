<script setup>
import Card from './components/Card.vue';
import Card2 from './components/Card2.vue';
import ExpandBox from './components/ExpandBox.vue';

</script>

<template>
  <div>
    <Card2>
      <p>Body</p>
      <template #header>
        <h1>Header</h1>
      </template>
      <template #footer>
        <p>Footer</p>
      </template>
    </Card2>

    <Card title="Título do card">
      <p>Conteúdo do card</p>
    </Card>


    <ExpandBox title="Caixa 1" content="Essa é a LOUD" />
    <expand-box title="Caixa 2" content="Então Isqueci" />

  </div>
</template>