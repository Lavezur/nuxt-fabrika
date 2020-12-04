<template>
  <div class="survey">
    <Params />

    <Questions />

    <Logic />

    <Respondents />

    <Conditions />
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
      activeItem: 'home'
    }
  }
}
</script>

<style lang="scss">
  .survey {
    margin-top: 40px;

    .survey__navigation {

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
