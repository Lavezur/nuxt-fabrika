<template>
  <div class="surveys">
    <Navigation />
    <div class="surveys__content">
      <Header />
      <button type="button" class="surveys__create-surveys" @click="compList = !compList">
        Добавить запрос
      </button>
      <hr>
      <surveyslist v-if="compList" />
      <survey v-else />
    </div>
  </div>
</template>

<script>
import Navigation from '@/components/navigation'
import Header from '@/components/header'
import Surveyslist from '@/components/surveyslist'
import Survey from '@/components/survey'
export default {
  name: 'Surveys',
  components: { Survey, Surveyslist, Header, Navigation },

  data () {
    return {
      compList: true
    }
  }
}
</script>

<style lang="scss">

.surveys {
  display: flex;
  flex-direction: row;

  .surveys__content {
    display: flex;
    flex-direction: column;
    width: 80%;
    margin: 0 auto;

      .surveys__create-surveys {
        margin: 18px 0 0;
        outline: none;
        cursor: pointer;
        text-transform: uppercase;
        background: none;
        border: 2px solid #ffa260;
        width: 248px;
        height: 52px;
        border-radius: 5px;
        background: {
          image: linear-gradient(90deg, #ffa260 50%, transparent 50%);
          position: 100%;
          size: 400%;
        }
        transition: background 420ms ease-in-out;

        &:hover {
          background-position: 0;
        }
      }

    > hr {
      border: none;
      margin-top: 30px;
      background-color: #b7b7b7;
      height: 1px;
    }
  }
}
</style>
