<template>
  <div class="screen-wrapper">
    <Search class="home__search" />
  </div>
</template>

<script>
  import Search from '@/components/Search';

  export default {
    components: {
      Search
    }
  }
</script>

<style scoped>
  .screen-wrapper {
    min-height: calc(100vh - 180px);
    padding: 24px;
    display: flex;
    justify-content: space-around;
    align-items: stretch;
  }
  .home__search {
    min-height: 320px;
    align-self: center;
  }
</style>

