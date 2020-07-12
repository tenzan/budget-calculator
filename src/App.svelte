<script>
  import Navbar from "./Navbar.svelte";
  import ExpensesList from "./ExpensesList.svelte";
  import expensesData from "./expenses";
  let expenses = [...expensesData];

  function removeExpense(id) {
    expenses = expenses.filter(item => item.id !== id);
  }
</script>

<Navbar />

<main class="content">
  <ExpensesList {expenses} {removeExpense} />
</main>
