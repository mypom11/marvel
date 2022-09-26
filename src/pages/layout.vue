<template>
  <div>
    <AppHeader />
    <h2>CHOOSE <br />YOUR CHARACTER</h2>
    <CharacterList />
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import CharacterList from "./characterList.vue";
export default {
  name: "LayOut",
  components: { AppHeader, CharacterList },
};
</script>

<style lang="scss" scoped>
@import "~@/assets/scss/_variables.scss";
h2 {
  padding: 100px 100px 20px;
  font-size: 40px;
  line-height: 1.5;
  font-weight: 600;
  @keyframes liner {
    from {
      width: 0;
    }
    to {
      width: 100%;
    }
  }
  &:after {
    display: block;
    content: "";
    height: 2px;
    width: 0;
    animation: liner 1s forwards;
    background: $red;
    margin-top: 10px;
  }
}
</style>
