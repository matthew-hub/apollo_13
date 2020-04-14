<template>
  <div class="phase-box">
    <div class="phase-number">Phase {{ phase.phase }}:</div>
    <div class="phase-additional" v-if="phase.additional">{{ phase.additional }}</div>
    <div class="phase-description">{{ phase.description }}</div>
  </div>
</template>

<script>
export default {
  name: "Phase",
  props: {
    phase: {
      type: Object,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
.phase-box {
  color: #202020;
  .phase-number {
    font-size: 2rem;
    font-family: BlackHanSans;
  }
  .phase-additional {
    font-family: Anton;
    font-size: 1.8rem;
  }
  .phase-description {
    color: #181818;
    font-family: OpenSans;
    font-size: 1.8rem;
  }
}
</style>
