<template>
  <div>
    <h1>To Do List</h1>
    <form>
      <input type="text" placeholder="Entre com a uma tarefa..." />
      <button>Enviar</button>
    </form>
  </div>
  <div class="to-do-list">
    <ol>
      <li>
        <span class="text">Tarefa 01</span>
        <span class="actions">
          <button class="complete">&#10004;</button>
          <button class="remove">&#10006;</button>
        </span>
      </li>
    </ol>
  </div>
</template>
<script>
export default {};
</script>
<style>

</style>
