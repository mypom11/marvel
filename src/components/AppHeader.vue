<template>
  <header>
    <div class="menu"><font-awesome-icon :icon="['fas', 'bars']" /></div>
    <h1>MARVEL</h1>
    <div class="people"><font-awesome-icon :icon="['fas', 'user']" /></div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style lang="scss" scoped>
@import "~@/assets/scss/_variables.scss";
header {
  @include flex;
  height: 60px;
  padding: 0 100px;
  > div {
    font-size: 24px;
    cursor: pointer;
    transition: 0.2s;
    &:hover {
      color: $teal;
    }
  }
  h1 {
    font-size: 24px;
    font-weight: 700;
  }
}
</style>
