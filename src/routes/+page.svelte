<script>
  //   import Compteur from "../components/Compteur.svelte";
  import UserCard from "../components/UserCard.svelte";

  const users = [
    { name: "Default Name", age: 0, email: "default@example.com", note: 12 },
    { name: "Alice", age: 30, email: "alice@example.com", note: 13 },
    { name: "Billal", age: 27, email: "alice@example.com", note: 9 },
  ];
</script>

<div class="container mt-4">
  <div class="row g-4">
    {#each users as u}
      {#if u.note > 10}
        <div class="col-md-6">
          <UserCard user={u} />
        </div>
      {/if}
    {/each}
  </div>
</div>
