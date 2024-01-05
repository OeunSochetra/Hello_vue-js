<script setup lang="ts">
export interface ITransaction {
  id: number;
  amount: number;
  text: string;
}

const transaction: ITransaction[] = [
  { id: 1, text: "Flower", amount: 45.9 },
  { id: 1, text: "Book", amount: 12.9 },
  { id: 1, text: "Camera", amount: 89.9 },
  { id: 1, text: "Phone", amount: 100.9 },
];
</script>

<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <li
      v-for="items in transaction"
      v-bind:key="items.id"
      :class="items.amount > 0 ? 'minus' : 'plus'"
    >
      {{ items.text }} <span>-${{ items.amount }}</span>
      <button class="delete-btn">x</button>
    </li>
    <li class="plus">
      Paycheck <span>$800</span>
      <button class="delete-btn">x</button>
    </li>
  </ul>
</template>

<style scoped></style>
