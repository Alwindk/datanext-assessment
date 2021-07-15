<template>
  <div class="container">
    <Forecasts :forecasts="forecasts" />
  </div>
  <div></div>
</template>

<script>
import Forecasts from "./Forecasts.vue";

export default {
  name: "App",
  components: {
    Forecasts
  },
  data() {
    return {
      forecasts: [],
      tempMin: "",
      tempMax: ""
    };
  },

  methods: {
    async fetchForecasts() {
      const res = await fetch("api/forecasts");

      const data = await res.json();

      return data;
    }
  },
  async created() {
    this.forecasts = await this.fetchForecasts();
  }
};
</script>

<style>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-content: center;
}
</style>
