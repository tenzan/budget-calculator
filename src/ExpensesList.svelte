<script>
  import SectionTitle from "./Title.svelte";
  import Expense from "./Expense.svelte";
  export let expenses = [];
</script>

<style>
  h2 {
    text-transform: capitalize;
  }
</style>

<section>
  <SectionTitle title="expense list" />
  {#each expenses as expense, index}
    <Expense {...expense} />
  {:else}
    <h2>currently you have no expenses</h2>
  {/each}
</section>
