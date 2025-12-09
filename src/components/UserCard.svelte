<script>
  export let name;
  export let age;
  export let email;
  export let note = 0;
</script>

<div class="user-card">
  <h2>{name}</h2>
  <p>Age: {age}</p>
  <p>Email: {email}</p>

  {#if note > 10}
    <p>Note: {note}</p>
  {/if}
</div>

<style>
  .user-card {
    border: 1px solid #ccc;
    padding: 1rem;
    border-radius: 0.5rem;
    max-width: 300px;
  }
</style>
