<template>
  <div class="fact-box">
    <div class="fact-text">{{ fact.fact }}</div>
    <div class="fact-description">{{ fact.description }}</div>
  </div>
</template>

<script>
export default {
  name: "Fact",
  props: {
    fact: {
      type: Object,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
.fact-box {
  color: #202020;
  .fact-text {
    font-family: Anton;
    font-size: 1.8rem;
  }
  .fact-description {
    // color: #181818;
    font-family: BlackHanSans;
    font-size: 1.8rem;
  }
}
</style>
