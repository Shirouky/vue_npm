<template>
  <div class="app">
    <div class="informer-container">
      <div class="flex-break"></div>
      <Temperature :temp_real="temp_real" :temp_feel="temp_feel" />

      <div class="wrap">
        <Humidity :hum="hum" />

        <div class="vertical-divider"></div>

        <Wind :wind="wind" />
      </div>
    </div>
  </div>
</template>

<script>
import Temperature from "./components/Temperature.vue";
import Humidity from "./components/Humidity.vue";
import Wind from "./components/Wind.vue";

export default {
  name: "FirstComponent",
  components: {
    Temperature,
    Humidity,
    Wind,
  },
  data() {
    return {
      temp_real: 1,
      temp_feel: -3.2,
      hum: 6,
      wind: 20,
    };
  },
};
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

.flex-break {
  flex-basis: 100%;
  height: 0;
}

.vertical-divider {
  height: 70px;
  width: 1px;
  background-color: #fff;
  vertical-align: middle;
  display: table-cell;
}

.app {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: rgb(244, 123, 186);
  background: linear-gradient(
    -25deg,
    rgba(244, 123, 186, 0.5) 20%,
    rgba(90, 95, 245, 0.5) 80%
  );
}

.wrap{
  display: flex;
  justify-content: space-around;
}
</style>
