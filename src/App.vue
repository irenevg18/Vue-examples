<template>
  <!-- // 1 - utilizar el componente en el template (imprimirlo)-->
  <Bank />

  <!-- ------------------------COUNTER--------------------------------- -->
  <!-- <div class="flex flex-col gap-4 items-center">
<div class="text-indigo-500 font-extrabold text-xl mt-10">Counter</div>

<!- <HelloWorld /> -->
  <!-- <input type="number" v-model.number="max1" class="border text-center" />
<Counter :max= "max1"/>
<Counter :max= "10"/>
<Counter :max= "20"/>
</div> -->
  <!-- ------------------------COUNTER--------------------------------- -->
</template>

<script>
// 1 - importar el componente
import HelloWorld from "./components/HelloWorld.vue";
import Counter from "./components/Counter.vue";
import Bank from "./components/Bank.vue";

export default {
  // 2 - registrar el componente
  components: {
    HelloWorld,
    Counter,
    Bank,
  },
  // <!-- ------------------------COUNTER--------------------------------- -->
  // data() {
  //   return{
  //   max1: 10,
  //   }
  // }
  // <!-- ------------------------COUNTER--------------------------------- -->
};
</script>

<style></style>
