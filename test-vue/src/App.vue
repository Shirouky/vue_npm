<template>
  <div class="informer-container">
    <div class="flex-break"></div>
    <Temperature temp_real="3.2" temp_feel="1.2" />

    <Humidity hum="13" />

    <div class="vertical-divider"></div>

    <Wind wind="14" />
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

.flex-break{
  flex-basis: 100%;
  height: 0;
}

.vertical-divider{
  height: 70px;
  width: 1px;
  background-color: #fff;
  vertical-align: middle;
  display: table-cell;
}
</style>
