<template>
  <vue-gauge
    :refid="'clusters-gauge-id'"
    :options="{
      'arcDelimiters': [85],
      'hasNeedle': false,
      'arcColors': ['#00FF00', '#d8d8d8'],
      'arcLabels': ['85%'],
      'rangeLabel': ['0%','100%'],
      'chartWidth': 275,
    }" />
</template>

<script>
import VueGauge from 'vue-gauge';

export default {
  name: 'ClustersGauge',
  components: { VueGauge }
}
</script>

<style scoped>
</style>
