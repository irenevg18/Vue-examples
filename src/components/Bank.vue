<template>
  <h1>Bank</h1>
  <div>income: {{ income }}€</div>
  <div>outcome: {{ outcome }}€</div>
  <div>balance: {{ balance }}€</div>

  <input type="text" class="border pl-2" v-model="name" placeholder="Name" />
  <input
    type="number"
    class="border pl-2"
    v-model="amount"
    placeholder="Amount"
  />

  <button
    class="border text-center text-white bg-slate-900 rounded px-6 py-2"
    @click="addItem"
  >
    Add
  </button>
  <ul>
    <li v-for="(item, i) in items" :key="i">
      {{ item.name }}: {{ item.amount }}€
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      outcome: -20,
      name: "",
      amount: 0,
      items: [],
    };
  },
  computed: {
    income() {
      return this.items
        .filter((item) => item.amount > 0)
        .reduce((acc, item) => acc + item.amount, 0);
    },
    outcome() {
      return this.items
        .filter((item) => item.amount < 0)
        .reduce((acc, item) => acc + item.amount, 0);
    },

    balance() {
      return this.income + this.outcome;
    },
  },
  methods: {
    addItem() {
      return this.items.push({
        name: this.name,
        amount: this.amount,
      });
    },
  },
};
</script>

<style></style>
