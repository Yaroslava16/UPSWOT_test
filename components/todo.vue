<template>
  <div class="todo-wrap">
    <div class="todo-wrap__title">
      <p>Your tasks:</p>
      <button class="todo-wrap__add-btn" @click="addTask">+</button>
    </div>
    <ul class="todo-wrap__list">
      <li class="todo-wrap__item" v-for="(task, i) in todoList" :key="i">
        {{ task.text }}
        <div class="todo-wrap__item-btn-wrap">
          <button class="todo-wrap__item-btn">
            <img src="~/assets/edit_icon.svg" alt="" />
          </button>
          <button class="todo-wrap__item-btn" @click="removeTask(i)">
            <img src="~/assets/remove_icon.svg" alt="" />
          </button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTask: {
        text: "new task",
      },
      todoList: [
        {
          text: "11111111111111111111111111111111111111111111111111111",
        },
        {
          text: "222222222222222222222222222222222222222222222222222222222222222222222",
        },
        {
          text: "333333333333333333333333333333333333333333333333333333333333333333333333333333333333333",
        },
        {
          text: "44444444444444444444444444",
        },
        {
          text: "5555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555",
        },
        {
          text: "666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666",
        },
      ],
    };
  },
  methods: {
    addTask() {
      this.todoList.unshift(this.newTask);
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
    display: flex;
    justify-content: space-between;
    padding: 0.5vw 0.5vw 0;
    font-weight: 500;
    font-size: 1.5vw;
    line-height: 3vw;
    border-bottom: 2px solid #fff;
    word-break: break-all;
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
      display: flex;
      margin-left: 2vw;
      padding: 0.5vw;
      right: 0;
    }
  }
}
</style>
