<template>
  <div class="help">
    <div class="help__wrapper">
      <div class="help__header">
        <div class="help__close" @click="closePopup" />
        <h3>У вас возникли вопросы ?</h3>
        <p>Напишите нам и мы обязательно свяжемся с вами !</p>
      </div>
      <form class="help__form" action="" onsubmit="return false;">
        <label class="help__label">
          <input class="help__input" type="text" placeholder="Имя">
        </label>
        <label class="help__label help__label-top">
          <input class="help__input" type="email" placeholder="Почта">
        </label>
        <button class="help__button">
          <span />
          <span />
          <span />
          <span />
          Отправить
        </button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Help',
  methods: {
    closePopup () {
      this.$emit('closePopup')
    }
  }
}
</script>

<style lang="scss">
  .help {
    min-width: 100%;
    min-height: 100%;
    position: fixed;
    z-index: 100;
    background: rgba(0, 0, 0, 0.5);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: visibility 0.5s linear, opacity 0.5s;

    .help__wrapper {
      max-width: 650px;
      width: 100%;
      height: 520px;
      background-color: white;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      position: fixed;
      box-sizing: border-box;
      border-radius: 10px;

      .help__header {
        text-align: center;
        color: #585858;
        display: flex;
        flex-direction: column;

        .help__close {
          background: url("../assets/icons/close.svg") top left / cover no-repeat;
          width: 20px;
          height: 20px;
          align-self: flex-end;
          margin: 15px 15px 0 0;
          cursor: pointer;
        }

        >h3 {
          font-size: 32px;
          letter-spacing: 2px;
          margin-top: 50px;
        }

        >p {
          padding-top: 15px;
        }
      }

      .help__form {
        max-width: 70%;
        margin: 50px auto 0;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        .help__label {
          border-bottom: 1px solid grey;

          .help__input {
            max-width: 600px;
            width: 100%;
            height: 45px;
            padding: 0 0 0 15px;
            border: none;
            outline: none;
            font-size: 16px;
            background-color: rgba(250, 250, 250, 0);
            color: grey;
          }
        }

        .help__label-top {
          margin-top: 20px;
        }

        .help__button {
          margin-top: 50px;
          width: 310px;
          height: 50px;
          position: relative;
          display: inline-block;
          text-transform: uppercase;
          color: black;
          font-size: 21px;
          border: none;
          background-color: white;
          letter-spacing: 2px;
          cursor: pointer;
          align-self: center;
          text-align: center;
          outline: none;

          &:hover {
            background-color: #b7b7b7;
            transition: 0.5s;
            transition-delay: 0.50s;
            color: #282828;
          }

          > span {
            position: absolute;
            display: block;
            background-color: black;
          }

          > span:nth-child(1) {
            left: 0;
            bottom: 0;
            width: 1px;
            height: 100%;
            transform: scaleY(0);
            transform-origin: top;
            transition: transform 0.10s;
          }

          &:hover > span:nth-child(1) {
            transform: scaleY(1);
            transform-origin: bottom;
            transition: transform 0.10s;
          }

          > span:nth-child(2) {
            left: 0;
            top: 0;
            width: 100%;
            height: 1px;
            transform: scaleX(0);
            transform-origin: right;
            transition: transform 0.10s;
            transition-delay: 0.10s;
          }

          &:hover > span:nth-child(2) {
            transform: scaleX(1);
            transform-origin: left;
            transition: transform 0.10s;
            transition-delay: 0.10s;
          }

          > span:nth-child(3) {
            right: 0;
            bottom: 0;
            width: 1px;
            height: 100%;
            transform: scaleY(0);
            transform-origin: bottom;
            transition: transform 0.10s;
            transition-delay: 0.20s;
          }

          &:hover > span:nth-child(3) {
            transform: scaleY(1);
            transform-origin: top;
            transition: transform 0.10s;
            transition-delay: 0.20s;
          }

          > span:nth-child(4) {
            left: 0;
            bottom: 0;
            width: 100%;
            height: 1px;
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.10s;
            transition-delay: 0.30s;
          }

          &:hover > span:nth-child(4) {
            transform: scaleX(1);
            transform-origin: right;
            transition: transform 0.10s;
            transition-delay: 0.30s;
          }
        }
      }
    }
  }
</style>
