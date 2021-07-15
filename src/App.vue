<template>
  <ForecastLayout />
</template>

<script>
import ForecastLayout from "./components/ForecastLayout.vue";

export default {
  name: "App",
  components: {
    ForecastLayout
  }
};
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
  padding: 0;
  background-color: rgb(199, 202, 206);
}
</style>
