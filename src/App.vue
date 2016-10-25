<template>
  <div id="app">
    <app-bar></app-bar>
    <monthly-ec2-cost></monthly-ec2-cost>
    <monthly-ec2-cost></monthly-ec2-cost>
  </div>
</template>

<script>
import AppBar from './components/shared/AppBar';
import MonthlyEc2Cost from './components/charts/MonthlyEc2Cost';

export default {
  name: 'app',
  components: {
    AppBar,
    MonthlyEc2Cost,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

body, html, main, .main, .app, app {
  margin: 0;
  min-height: 100%;
  height: 100%;
  background-color: #efefef;
}

body {
  font-family: 'Roboto', sans-serif;
}

.echarts {
  height: 250px;
  width: 500px;
  display: inline-block;
  margin: 10px;
}
</style>
