<template>
  <div class="bg-rose-400 text-yellow-500">The count is: {{ count }}</div>
  <button class="border px-4 py-2 rounded" @click="count++">+1</button>
</template>

<script>
export default {
data() {
    return {
      
      
      
      count: 0,
    };
  },
};
</script>
