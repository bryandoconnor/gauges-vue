<template>
  <vue-gauge
    :refid="'cpu-gauge-id'"
    :options="{
      'arcDelimiters': [45],
      'hasNeedle': false,
      'arcColors': ['#ffff00', '#d8d8d8'],
      'arcLabels': ['45%'],
      'rangeLabel': ['0%','100%'],
      'chartWidth': 275,
    }" />
</template>

<script>
import VueGauge from 'vue-gauge';

export default {
  name: 'CPUsGauge',
  components: { VueGauge }
}
</script>

<style scoped>

</style>