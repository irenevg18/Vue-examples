<template>

<div class="flex flex-col items-center">
<div class="text-indigo-500 font-extrabold text-xl mt-10">Counter</div>

<!-- <HelloWorld /> -->
<input type="number" v-model.number="max1" class="border" />
<Counter :max= "max1"/>
<Counter :max= "10"/>
<Counter :max= "20"/>
</div>
</template>


<script>
import HelloWorld from "./components/HelloWorld.vue";
import Counter from "./components/Counter.vue";

export default {
  components: {
    HelloWorld,
    Counter,
  },
  data() {
    return{
    max1: 10,
    }
  }
};

</script>

<style>
</style>
