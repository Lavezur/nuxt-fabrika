<template>
  <div class="survey">
    <div class="survey__navigation">
      <button class="survey__button" @click="setCop('Params')">
        Параметры
      </button>
      <button class="survey__button" @click="setCop('Questions')">
        Вопросы
      </button>
      <button class="survey__button" @click="setCop('Logic')">
        Логика
      </button>
      <button class="survey__button" @click="setCop('Respondents')">
        Респонденты
      </button>
      <button class="survey__button" @click="setCop('Conditions')">
        Условия
      </button>
    </div>
    <keep-alive>
      <component :is="component" />
    </keep-alive>
  </div>
</template>

<script>
import Params from '@/components/params'
import Questions from '@/components/questions'
import Logic from '@/components/logic'
import Respondents from '@/components/respondents'
import Conditions from '@/components/conditions'
export default {
  name: 'Survey',
  components: { Conditions, Respondents, Logic, Questions, Params },
  data () {
    return {
      component: 'Params'
    }
  },
  methods: {
    setCop (value) {
      this.component = value
    }
  }
}
</script>

<style lang="scss">
  .survey {
    margin-top: 40px;

    .survey__navigation {
      display: flex;
      justify-content: space-between;

      .survey__button {
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
