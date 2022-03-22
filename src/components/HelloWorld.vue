<template>
<h1 class="bg-rose-400
">{{message}}</h1>
<input type="text" v-model="message"/>
</template>

<script>
export default {
  data() {
    return {
      message: "",
      };
    },
};

</script>

<style>
</style>
