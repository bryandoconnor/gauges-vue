<template>
  <vue-gauge
    :refid="'pods-gauge-id'"
    :options="{
      'arcDelimiters': [24],
      'hasNeedle': false,
      'arcColors': ['#ff0000', '#d8d8d8'],
      'arcLabels': ['24%'],
      'rangeLabel': ['0%','100%'],
      'chartWidth': 275,
    }" />
</template>

<script>
import VueGauge from 'vue-gauge';

export default {
  name: 'PodsGauge',
  components: { VueGauge },
  setup() {
    return {
      UtilNum: 20
    }
  }
}
</script>

<style scoped>

</style>
