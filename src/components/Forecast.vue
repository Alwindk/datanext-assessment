<template>
  <div class="forecast">
    <p>{{ forecast.date }} {{ forecast.time }}</p>
    <p class="temp">{{ forecast.temp }}°</p>
    <p class="type">{{ forecast.type }}</p>
  </div>
</template>

<script>
export default {
  name: "Forecast",
  props: {
    forecast: Object
  }
};
</script>

<style scoped>
.forecast {
  font-family: Arial, Helvetica, sans-serif;
  display: flex;
  flex-direction: column;
  background-color: white;
  align-items: center;
  font-size: 1em;
}

.type {
  font-style: italic;
  font-size: 0.95em;
  margin-bottom: 35px;
}

.temp {
  font-weight: bold;
  margin-top: -12px;
  margin-bottom: -15px;
}

.tempMax {
  font-weight: bold;
  margin-top: -12px;
  margin-bottom: -15px;
  color: orange;
}

.tempMin {
  font-weight: bold;
  margin-top: -12px;
  margin-bottom: -15px;
  color: blue;
}
</style>
