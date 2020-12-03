<template>
  <div class="header">
    <div class="header__input-wrapper">
      <input class="header__input" type="text" placeholder="Поиск по системе">
      <div class="header__input-find-button" />
    </div>
    <div class="header__profile">
      <img src="https://w-dog.ru/wallpapers/5/18/289291145046987/evropejskaya-koshka-dikij-kot-morda-vzglyad.jpg" alt="Кот" class="header__avatar">
      <div class="header__profile-data">
        <h3 class="header__profile-name">
          Кот
        </h3>
        <p class="header__workplace">
          Youtube
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss">
  .header {
    display: flex;
    flex-direction: row;
    width: 100%;
    margin: 40px auto;
    height: fit-content;
    justify-content: space-between;
    align-items: center;

    .header__input-wrapper {
      display: flex;
      height: fit-content;
      max-width: 50%;
      width: 100%;
      border: 1.5px solid #b7b7b7;
      border-radius: 5px;
      justify-content: space-between;

      .header__input {
        width: 100%;
        padding: 0 0 0 15px;
        font-size: 16px;
        height: 30px;
        border: none;
        align-self: flex-end;
        outline: none;
        border-radius: 5px;
      }

      .header__input-find-button {
        background: url("../assets/icons/loupe.svg") top left / cover no-repeat;
        width: 18px;
        height: 17px;
        align-self: center;
        margin-right: 10px;
        cursor: pointer;
      }
    }

    .header__profile {
      display: flex;
      height: 50px;
      align-items: center;

      .header__avatar {
        width: 45px;
        height: 45px;
        object-fit: cover;
        border-radius: 50%;
      }

      .header__profile-data {
        margin-left: 10px;

        .header__profile-name {

        }

        .header__workplace {
          font-size: 12px;
          color: #8e8d8d;
        }
      }
    }
  }
</style>
