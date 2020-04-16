<template>
  <main>
    <div class="main-wrapper">
      <div class="phases-wrapper">
        <div class="phases-wrapper__left">
          <div v-for="phase in phases.slice(0, phases.length / 2)" v-bind:key="phase.id">
            <Phase v-bind:phase="phase" />
          </div>
        </div>
        <div class="phases-wrapper__right">
          <div v-for="phase in phases.slice(phases.length / 2)" v-bind:key="phase.id">
            <Phase v-bind:phase="phase" />
          </div>
        </div>
      </div>
      <h3>APOLLO 13 FACTS</h3>
      <div class="facts-wrapper">
        <div class="facts-wrapper__left">
          <div v-for="fact in facts.slice(0, facts.length / 2 + 1)" v-bind:key="fact.id">
            <Fact v-bind:fact="fact" />
          </div>
        </div>
        <div class="facts-wrapper__right">
          <div v-for="fact in facts.slice(facts.length / 2 + 1)" v-bind:key="fact.id">
            <Fact v-bind:fact="fact" />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Phase from "../Phase.vue";
import Fact from "../Fact.vue";

export default {
  name: "Main",
  components: {
    Phase,
    Fact
  },
  props: {
    phases: {
      type: Array,
      required: true
    },
    facts: {
      type: Array,
      required: true
    }
  }
};
</script>

<style lang="scss">
.main-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto auto;
  grid-row-gap: 30px;

  h3 {
    color: #202020;
    font-family: Ultra;
    font-size: 3rem;
  }

  @media (min-width: 940px) {
    h3 {
      text-align: center;
    }
  }
}
.phases-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-row: auto;
  justify-content: space-between;
  padding-bottom: 40px;
  @media (min-width: 940px) {
    grid-template-columns: 350px 350px;
    grid-column-gap: 50px;
  }

  &__left,
  &__right {
    display: grid;
    grid-template-columns: 1fr;
    grid-row: auto;
    grid-row-gap: 35px;
  }

  &__right {
    align-content: center;
  }
}

.facts-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: fill auto auto;
  justify-content: space-between;
  grid-row-gap: 20px;

  @media (min-width: 940px) {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: fill auto auto;
    grid-column-gap: 50px;
  }

  &__left,
  &__right {
    display: grid;
    grid-template-columns: 1fr;
    grid-row: auto;
    grid-row-gap: 25px;
  }
}
</style>
