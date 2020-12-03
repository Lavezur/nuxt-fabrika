<template>
  <div class="call-center">
    <Navigation />
    <div class="call-center__content">
      <Header />
      <h1>Тут колл-центр</h1>
    </div>
  </div>
</template>

<script>
import Navigation from '@/components/navigation'
import Header from '@/components/header'
export default {
  name: 'Callcenter',
  components: { Header, Navigation }
}
</script>

<style lang="scss">

.call-center {
  display: flex;
  flex-direction: row;

  .call-center__content {
    display: flex;
    flex-direction: column;
    width: 80%;
    margin: 0 auto;
  }
}

</style>
