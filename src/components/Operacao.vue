<script setup>
  const props = defineProps(['operacao', 'num1', 'num2'])
</script>

<template>
  <div class="operation">
    <h2>Seleciona e operação para o resultado</h2>
    <select @change="props.operacao">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">*</option>
      <option value="/">/</option>
    </select>
  </div>
  <div>
    <input @keyup="props.num1" required type="number" placeholder="Digite o N."/>
    <input @keyup="props.num2" required type="number" placeholder="Digite o N."/>
  </div>

</template>

<style>
  input {
    margin: 30px;
    padding: 4px;
    border-radius: 4px;
  }
</style>