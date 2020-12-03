<template>
  <div class="navigation">
    <help
      v-if="isPopupVisible"
      @closePopup="closePopup"
    />
    <router-link tag="button" to="/" class="navigation__logo">
      LOGO
    </router-link>
    <div class="navigation__buttons">
      <router-link tag="button" to="/surveys" class="navigation__button">
        <img src="../assets/icons/surveys.svg" alt="survey" class="navigation__button-icon">
        <p class="navigation__button-text">
          Опросы
        </p>
      </router-link>
      <router-link tag="button" to="/users" class="navigation__button">
        <img src="../assets/icons/avatars.svg" alt="avatars" class="navigation__button-icon">
        <p class="navigation__button-text">
          Пользователи
        </p>
      </router-link>
      <router-link tag="button" to="/blacklist" class="navigation__button">
        <img src="../assets/icons/blacklist.svg" alt="blacklist" class="navigation__button-icon">
        <p class="navigation__button-text">
          Черные списки
        </p>
      </router-link>
      <router-link tag="button" to="/call-center" class="navigation__button">
        <img src="../assets/icons/callcenter.svg" alt="callcenter" class="navigation__button-icon">
        <p class="navigation__button-text">
          Колл-центр
        </p>
      </router-link>
    </div>
    <div class="navigation__question" @click="showPopup" />
  </div>
</template>

<script>
import Help from '@/components/help'
export default {
  name: 'Navigation',
  components: { Help },
  data () {
    return {
      isPopupVisible: false
    }
  },

  methods: {
    showPopup () {
      this.isPopupVisible = true
    },
    closePopup () {
      this.isPopupVisible = false
    }
  }
}
</script>

<style lang="scss">

.navigation {
  max-width: 100px;
  height: 800px;
  border-right: 1px solid #b7b7b7;
  display: grid;
  grid-template-rows: min-content auto auto;

    .navigation__logo {
      width: 50px;
      height: 50px;
      background-color: red;
      border-radius: 50%;
      margin: 20px auto 0;
      text-align: center;
      color: white;
      cursor: pointer;
      outline: none;
      border: none;
    }

    .navigation__buttons {
      display: flex;
      flex-direction: column;
      max-height: 380px;
      margin-top: 80px;
      height: 100%;
      justify-content: space-between;

      .navigation__button {
        display: flex;
        flex-direction: column;
        align-items: center;
        cursor: pointer;
        justify-content: center;
        height: 85px;
        background-color: white;
        outline: none;
        border: none;

        &:hover {
          background-color: #e2e2e2;
        }

        .navigation__button-icon {
          width: 35px;
          height: 35px;
        }

        .navigation__button-text{
          padding-top: 10px;
          font-size: 11px;
        }
      }
    }

    .navigation__question {
      background: url("../assets/icons/problem.png") top left / cover no-repeat;
      width: 50px;
      height: 50px;
      margin: 0 auto 50px;
      align-self: end;
      cursor: pointer;
    }
}

</style>
