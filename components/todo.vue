<template>
  <div class="todo-wrap">
    <div class="todo-wrap__title">
      <p>Your tasks:</p>
      <button class="todo-wrap__add-btn">+</button>
    </div>
    <ul class="todo-wrap__list">
      <li class="todo-wrap__item" v-for="(task, i) in todoList" :key="i">
        {{ task.text }}
      </li>
      <!-- <li class="todo-wrap__item">2222222</li>
      <li class="todo-wrap__item">3333333333</li> -->
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
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
  // props: {
  //   todoList: [],
  // },
};
</script>

<style lang="scss" scoped>
.todo-wrap {
  width: 33vw;
  margin: 0 auto;

  border-radius: 0.6vw;
  background-color: #e1e9ff;
  &__add-btn {
    position: absolute;
    top: 2.5vw;
    right: 2vw;
    display: flex;
    align-items: center;
    justify-content: center;

    width: 3vw;
    height: 3vw;

    border-radius: 50%;
    background-color: #2f62f1;
    color: #fff;
    font-size: 2vw;
    cursor: pointer;
  }
  &__title {
    position: relative;
    padding: 0.6vw;
    height: 4.167vw;
    background-color: #0095ff82;
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
    padding: 1vw;
  }
  &__item {
    padding: 0.5vw 0.5vw 0;
    font-weight: 500;
    font-size: 1.5vw;
    line-height: 3vw;
    border-bottom: 2px solid #fff;
    word-break: break-all;
  }
}
</style>
