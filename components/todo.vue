<template>
  <div class="todo-wrap">
    <div class="todo-wrap__title">
      <p>Your tasks:</p>
      <button class="todo-wrap__add-btn" @click="addTask">+</button>
    </div>
    <ul class="todo-wrap__list">
      <li class="todo-wrap__item" v-for="(task, i) in todoList" :key="i">
        <p>{{ task.text }}</p>
        <div class="todo-wrap__item-btn-wrap">
          <button class="todo-wrap__item-btn" @click="editTask(i)">
            <img src="~/assets/edit_icon.svg" alt="" />
          </button>
          <button class="todo-wrap__item-btn" @click="removeTask(i)">
            <img src="~/assets/remove_icon.svg" alt="" />
          </button>
        </div>
      </li>
    </ul>
    <input
      class="todo-wrap__input"
      v-if="editInput"
      type="text"
      v-model="newTask.text"
      v-on:keyup.enter="editInput = !editInput"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      editInput: false,
      newTask: {
        text: "",
      },
      todoList: [],
    };
  },
  methods: {
    addTask() {
      this.editInput = true;
      this.todoList.unshift(this.newTask);
      this.newTask.text = " ";
    },
    editTask(i) {
      for (const task in this.todoList) {
        if (task == i) {
          this.editInput = true;
        }
      }
    },
    removeTask(i) {
      this.todoList.splice(i, 1);
    },
  },
};
</script>

<style lang="scss" scoped>
.todo-wrap {
  width: 52vw;
  height: 29vw;
  margin: 0 auto;
  border-radius: 0.6vw;
  background-color: #e1e9ff;
  overflow-y: scroll;

  &__add-btn {
    position: absolute;
    top: 2.5vw;
    right: 4.3vw;
    display: flex;
    align-items: center;
    justify-content: center;

    width: 3vw;
    height: 3vw;

    border-radius: 50%;
    background-color: #fff;
    color: rgb(240, 9, 9);
    font-weight: 600;
    font-size: 2.11vw;
    transition-duration: 0.5s;

    cursor: pointer;
    &:hover {
      color: #fff;
      background-color: rgb(240, 9, 9);
    }
  }
  &__title {
    position: fixed;
    width: 50.7vw;
    padding: 0.6vw;
    height: 4.167vw;
    background-color: #00afed;
    font-size: 2vw;
    font-weight: 500;
    text-align: center;
    color: #fff;
    border-radius: 0.6vw;
    p {
      text-shadow: 0.2vw 0 0 #4074b5;
    }
  }
  &__list {
    padding: 5vw 1vw 1vw;
  }

  &__item {
    position: relative;
    display: flex;
    justify-content: space-between;
    padding: 3.5vw 0.5vw 0;
    font-weight: 500;
    font-size: 1.5vw;
    line-height: 3vw;
    border-bottom: 2px solid #fff;
    word-break: break-all;
    p {
      width: 82%;
    }

    &-btn {
      cursor: pointer;
      transition-duration: 0.5s;
      img {
        width: 2.5vw;
      }

      &:not(:last-child) {
        margin-right: 2vw;
      }

      &:hover,
      &:focus {
        transform: scale(1.2);
      }
    }
    &-btn-wrap {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      display: flex;
      margin-left: 2vw;
      padding: 0.5vw;
      right: 0;
    }
  }
  &__input {
    position: absolute;
    top: 31.8%;
    left: 14%;
    width: 60%;
    padding: 0.5vw;
    font-size: 1.5vw;
  }
}
</style>
