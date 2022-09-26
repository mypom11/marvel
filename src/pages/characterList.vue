<template>
  <main>
    <div class="list">
      <ul :style="{ left: `-${move * 220}px` }">
        <li>
          <img src="" alt="" />
        </li>
        <li>
          <img src="" alt="" />
        </li>
        <li>
          <img src="" alt="" />
        </li>
        <li>
          <img src="" alt="" />
        </li>
        <li>
          <img src="" alt="" />
        </li>
        <li>
          <img src="" alt="" />
        </li>
        <li>
          <img src="" alt="" />
        </li>
        <li>
          <img src="" alt="" />
        </li>
      </ul>
    </div>
    <div class="desc">
      <span @click="move--" :class="{ disabled: move === 0 }"
        ><font-awesome-icon :icon="['fas', 'arrow-left']"
      /></span>
      <span @click="move++" :class="{ disabled: move === 5 }"
        ><font-awesome-icon :icon="['fas', 'arrow-right']"
      /></span>
      <div class="sub">
        <h4>AVENGERS</h4>
        <p>
          The Avengers Fight Alien Monsters in Deep Space. Starring Iron Man,
          Ironheart, War Machine, and more! 'Avengers Unlimited Infinity Comic'
          #9
        </p>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "CharacterList",
  data() {
    return {
      move: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "~@/assets/scss/_variables.scss";

.list {
  margin: 0 100px 100px;
  overflow: hidden;
  height: 300px;
  > ul {
    @include flex(flex-start, stretch);
    position: relative;
    height: 100%;
    width: fit-content;
    gap: 20px;
    transition: 0.2s;
    > li {
      width: 200px;
      height: 100%;
    }
  }
}

.desc {
  padding: 0 100px;
  @include flex(flex-start);
  gap: 20px;
  span {
    width: 40px;
    height: 40px;
    @include flex(center, center);
    border-radius: 50%;
    border: 1px solid $white;
    font-size: 20px;
    transition: 0.2s;
    cursor: pointer;
    &.disabled {
      opacity: 0.5;
      pointer-events: none;
    }
    &:hover {
      color: $teal;
      border: 1px solid $teal;
    }
  }
  h4 {
    font-size: 20px;
    font-weight: 500;
    margin-bottom: 10px;
  }
  p {
    width: 600px;
    color: rgba($color: $white, $alpha: 0.6);
  }
}
</style>
