<template>
  <div class="index">
    <Navigation />
    <div class="index__content">
      <Header />
      <h1>Тут главная страница</h1>
    </div>
  </div>
</template>

<script>
import Navigation from '../components/navigation'
import Header from '../components/header'
export default {
  components: { Header, Navigation }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
}

.index {
  display: flex;
  flex-direction: row;

  .index__content {
    display: flex;
    flex-direction: column;
    width: 80%;
    margin: 0 auto;
  }
}

</style>
