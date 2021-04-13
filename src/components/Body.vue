<template>
  <div>
    <h1>To Do List</h1>
    <form @submit.prevent="save()">
      <input type="text" placeholder="Digite uma tarefa..." v-model="toDo" />
      <button type="submit">Enviar</button>
    </form>
    <p class="error-message" v-show="errorMessage">{{ errorMessage }}</p>
  </div>
  <div class="to-do-list">
    <ol>
      <li v-for="td in toDoList" :key="td.text">
        <span class="text" :class="{ completed: td.completed }">
          {{ td.text }}</span
        >
        <span class="actions">
          <button class="complete" @click="complete(td)">&#10004;</button>
          <button class="remove">&#10006;</button>
        </span>
      </li>
    </ol>
  </div>
</template>
<script>
export default {
  data() {
    return {
      errorMessage: null,
      toDoList: [
        { text: "Tarefa 01", completed: false },
        { text: "Tarefa 02", completed: true },
      ],
      toDo: "",
    };
  },
  methods: {
    save() {
      this.errorMessage = null;
      if (!this.toDo) {
        this.errorMessage = "Digite a tarefa!";
        return;
      }
      this.toDoList.push({ text: this.toDo, completed: false });
      this.toDo = "";
    },
    complete(td) {
      td.completed = true;
    },
  },
};
</script>
<style scoped>
h1 {
  text-align: center;
}

form {
  width: 100%;
  display: flex;
  border-radius: 3px;
  margin-bottom: 10px;
}

form input {
  width: 80%;
  border: 0;
  padding: 10px;
  border-top-left-radius: 3px;
  border-bottom-left-radius: 3px;
}

form button {
  width: 20%;
  border: 0;
  background-color: black;
  color: white;
  padding: 10px;
  border-top-right-radius: 3px;
  border-bottom-right-radius: 3px;
}

.error-message {
  color: rgb(248, 12, 12);
  margin-bottom: 10px;
  padding: 3px;
  margin: 10px 2px;
  background-color: #f1b2b2;
  border-radius: 3px;
  font-size: 0.8em;
}

.to-do-list ol {
  padding: 0;
  margin: 0;
}

.to-do-list ol li {
  border-top: 1px solid black;
  display: flex;
  justify-content: space-between;
}

.to-do-list ol li .text {
  max-width: cal(100% - 60px);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.to-do-list ol li .text.completed {
  text-decoration: line-through;
}

.to-do-list ol li .actions {
  width: 45px;
  display: flex;
  vertical-align: middle;
  height: 100%;
  justify-content: flex-end;
  margin-left: 3px;
}

.to-do-list ol li .actions button {
  width: 20px;
  margin: 3px 2px 3px 2px;
  height: 20px;
  line-height: 15px;
  border-radius: 10px;
  font-size: 13px;
  border: 1px solid #6b6767;
  background-color: transparent;
  cursor: pointer;
  outline: none;
}

.to-do-list ol li .actions button.complete {
  color: #12bd73;
  border: 1px solid #12bd73;
}
.to-do-list ol li .actions button.remove {
  margin-left: 5px;
  color: #e90d0d;
  border: 1px solid #e90d0d;

  cursor: pointer;
}
</style>
