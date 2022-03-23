<template>
<div class="bg-gray-100 w-screen flex flex-col items-center rounded p-2">
  <div>The count is: <span :class="{'text-red-500' :count === max, 'text-orange-300' :count >= max-3 && count < max, 'text-green-500' :count < max-3}"> {{ count }} </span></div>
  <div class="flex">
   <button class="border bg-white px-4 py-2 rounded" :class="{'text-gray-300' : count === 0}" :disabled= "count === 0" @click="decrease">-1</button>
  <button class="border bg-white px-4 py-2 rounded" :class="{'text-gray-300' : count === max}" :disabled= "count === max" @click="increase">+1</button>
  </div>
  </div>
</template>

<script>
export default {
props: ["max"],
data() {
    return {
      count: 0,
    };
  },
  methods: {
    decrease() {
      if (this.count > 0) this.count--;
    },
    increase() {
      if (this.count < this.max) this.count++;
    },
  },
};
</script>
