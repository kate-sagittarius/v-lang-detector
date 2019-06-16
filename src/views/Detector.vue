<template>
  <div class="screen-wrapper">
    <Search class="card"/>
    <Result class="card"/>
  </div>
</template>

<script>
  import Search from '@/components/Search';
  import Result from '@/components/Result';

  export default {
    components: {
      Search,
      Result
    }
  }
</script>

<style scoped>
  .screen-wrapper {
    min-height: calc(100vh - 180px);
    padding: 24px;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
  .card {
    height: 320px;
    width: 402px;
  }
</style>

