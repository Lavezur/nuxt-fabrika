<template>
  <div class="blacklist">
    <Navigation />
    <div class="blacklist__content">
      <Header />
      <h1>Тут черные списки</h1>
    </div>
  </div>
</template>

<script>
import Navigation from '@/components/navigation'
export default {
  name: 'Blacklist',
  components: { Navigation }
}
</script>

<style lang="scss">

.blacklist {
  display: flex;
  flex-direction: row;

  .blacklist__content {
    display: flex;
    flex-direction: column;
    width: 80%;
    margin: 0 auto;
  }
}

</style>
