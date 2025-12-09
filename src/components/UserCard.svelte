<script>
  import { Utils } from "$lib/utils";

  // export let name;
  // export let age;
  // export let email;
  // export let note = 0;
  export let user = {
    name: "Default Name",
    age: 0,
    email: "default@example.com",
  };

  if (!Utils.IsObject(user)) {
    throw new Error("is not a object");
  }
</script>

<div class="card">
  <div class="card-body">
    <h2 class="card-title">{user.name}</h2>
    <p class="card-text">Age: {user.age}</p>

    {#if user.note > 10}
      <p class="card-text"><strong>Note: {user.note}</strong></p>
    {/if}
  </div>
</div>
