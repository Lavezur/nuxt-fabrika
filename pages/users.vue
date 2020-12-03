<template>
  <div class="users">
    <Navigation />
    <div class="users__content">
      <Header />
      <h1>Тут пользователи</h1>
    </div>
  </div>
</template>

<script>
import Navigation from '@/components/navigation'
import Header from '@/components/header'
export default {
  name: 'Users',
  components: { Header, Navigation }
}
</script>

<style lang="scss">

.users {
  display: flex;
  flex-direction: row;

  .users__content {
    display: flex;
    flex-direction: column;
    width: 80%;
    margin: 0 auto;
  }
}

</style>
