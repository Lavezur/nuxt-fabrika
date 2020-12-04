<template>
  <div class="respondents">
    <div class="respondents__input-wrapper">
      <input type="text" class="respondents__input" placeholder="Добавить опрос">
    </div>
    <div class="respondents__add">
      <p class="respondents__add-text">
        Нажмите, чтобы добавить новое условие выборки. Все условия связываються между собой логическим "и"
      </p>
    </div>
    <div class="respondents__buttons">
      <button class="respondents__test">
        Протестировать опрос
      </button>
      <button class="respondents__next">
        Далее ->
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Respondents'
}
</script>

<style lang="scss">

.respondents {
  display: flex;
  flex-direction: column;
  margin-top: 40px;
  border-radius: 25px;
  box-shadow: 2px 1px 10px 0.1px rgba(0, 0, 0, 0.3);

  .respondents__input-wrapper {
    margin: 20px auto 10px;
    width: 95%;

    .respondents__input{
      width: 100%;
      border: none;
      padding-left: 20px;
      height: 40px;
      font-size: 14px;
      outline: none;
    }
  }

  .respondents__add {
    box-sizing: border-box;
    border: 1px solid #b7b7b7;
    display: flex;
    height: 70px;
    margin: 20px 10px;
    justify-content: center;
    cursor: pointer;

    .respondents__add-text {
      color: green;
      align-self: center;
      max-width: 470px;
    }
  }

  .respondents__buttons {
    display: flex;
    justify-content: space-between;
    width: 90%;
    margin: 15px auto;

    .respondents__test {
      color: green;
      padding: 10px;
      font-size: 12px;
      outline: none;
      border: #8e8d8d;
      width: fit-content;
      border-radius: 5px;
    }

    .respondents__next {
      color: white;
      padding: 10px;
      font-size: 12px;
      outline: none;
      background-color: green;
      border: none;
      border-radius: 5px;
    }
  }
}
</style>
