<script setup lang="ts">
import Header from "./components/Header.vue";
import Balance from "./components/Balance.vue";
import IncomeExpense from "./components/IncomeExpense.vue";
import TransactionList from "./components/TransactionList.vue";
import AddTransaction from "./components/AddTransaction.vue";
</script>

<template>
  <Header></Header>
  <div class="container">
    <Balance></Balance>
    <IncomeExpense></IncomeExpense>
    <TransactionList></TransactionList>
    <AddTransaction></AddTransaction>
  </div>
</template>

<style scoped></style>
