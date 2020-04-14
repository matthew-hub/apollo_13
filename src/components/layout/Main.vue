<template>
  <main>
    <div class="main-wrapper">
      <div class="phases-wrapper">
        <div v-for="phase in phases" v-bind:key="phase.id">
          <!-- <h3>{{ phase.id + 1 }}</h3> -->
          <Phase v-bind:phase="phase" />
        </div>
      </div>
      <div class="facts-wrapper">
        <h3>APOLLO 13 FACTS</h3>
        <div v-for="fact in facts" v-bind:key="fact.id">
          <Fact v-bind:fact="fact" />
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
  grid-row-gap: 50px;
}
.phases-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-row: auto;
  grid-row-gap: 35px;
}

.facts-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-row: auto;
  grid-row-gap: 20px;
  h3 {
    color: #202020;
    font-family: Ultra;
    font-size: 3rem;
  }
}
</style>
