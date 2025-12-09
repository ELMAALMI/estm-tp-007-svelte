<script>
  let todos = [];
  let input = "";

  function addTodo() {
    if (input.trim()) {
      todos = [...todos, { id: Date.now(), text: input }];
      input = "";
    }
  }

  function removeTodo(id) {
    todos = todos.filter((todo) => todo.id !== id);
  }
</script>

<div class="container mt-5">
  <h1 class="mb-4">Todo List</h1>

  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control"
      bind:value={input}
      placeholder="Add a todo..."
      on:keydown={(e) => e.key === "Enter" && addTodo()}
    />
    <button class="btn btn-primary" on:click={addTodo}>Add</button>
  </div>

  <ul class="list-group">
    {#each todos as todo (todo.id)}
      <li
        class="list-group-item d-flex justify-content-between align-items-center"
      >
        {todo.text}
        <button
          class="btn btn-sm btn-danger"
          on:click={() => removeTodo(todo.id)}
        >
          Remove
        </button>
      </li>
    {/each}
  </ul>
</div>
