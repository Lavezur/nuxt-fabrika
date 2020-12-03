<template>
  <div class="survey">
    <div class="survey__navigation">
      <button class="survey__params">
        Параметры
      </button>
      <button class="survey__params">
        Вопросы
      </button>
      <button class="survey__params">
        Логика
      </button>
      <button class="survey__params">
        Условия
      </button>
      <button class="survey__params">
        Респонденты
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Survey',
  data () {

  },
  props: {

  }
}
</script>

<style lang="scss">
  .survey {
    margin-top: 40px;

    .survey__navigation {
      display: flex;
      justify-content: space-between;

      .survey__params {
        border: none;
        outline: none;
        color: #ffa260;
        background-color: white;
        font-size: 16px;
        cursor: pointer;

        &:hover {
          color: #b7b7b7;
        }
      }
    }
  }
</style>
