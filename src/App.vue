<template>
  <div>
    <h1>Calculadora</h1>
    Numero1 : <input v-model.number="numero1" />
    Numero2 :  <input v-model.number="numero2"/>   
    <button @click="sumarnumero">Resultado</button>
 <p> Resultado: {{ suma }}</p>
  </div>
</template>


<script>
import { ref } from 'vue';

export default {
  setup() {
    const numero1 = ref('')
    const numero2 = ref('')
    const suma = ref('')

    function sumarnumero () {
      suma.value= numero1.value + numero2.value;
    }

    return {
      numero1,
      numero2,
      suma,
      sumarnumero
    };
  },
};
</script>
<style scoped>

body{
  background-color: aqua;
 }
</style>