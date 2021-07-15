<template>
  <div class="box" :key="forecast.id" v-for="forecast in forecasts">
    <Forecast :forecast="forecast" />
  </div>
</template>

<script>
import Forecast from "./Forecast";

export default {
  name: "Forecasts",
  props: {
    forecasts: Array
  },
  components: {
    Forecast
  }
};
</script>

<style scoped>
.box {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding-left: 50px;
  padding-right: 50px;
  border-radius: 10px;
  margin-top: 22%;
  background-color: white;
  box-shadow: 0px 0px 10px #acacac;
}

.cold {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding-left: 50px;
  padding-right: 50px;
  border-radius: 10px;
  margin-top: 22%;
  background-color: white;
  box-shadow: 0px 0px 10px #acacac;
  border: solid blue 3px;
}

.warm {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding-left: 50px;
  padding-right: 50px;
  border-radius: 10px;
  margin-top: 22%;
  background-color: white;
  box-shadow: 0px 0px 10px #acacac;
  border: solid orange 3px;
}
</style>
