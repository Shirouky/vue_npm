<template>
  <div class="informer-container">

      <div class="flex-break"></div>
      <Temperature temp_real="3.2" temp_feel="1.2"/>
      <div class="humidity">
        <img src="img/humidity.png"> 12 <small>%</small>
      </div>

      <div class="vertical-divider"></div>

      <div class="wind">
        <img src="img/wind.png"> 12 <small>м/с</small>
      </div>

    </div>
</template>

<script>

import Temperature from './components/Temperature.vue'

export default {
  name: 'FirstComponent',
  components: {
    Temperature
  }
}
</script>

<style>
.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  min-height: 255px;
  padding: 30px;
  background-image: url("../img/forest.png");
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}
</style>
