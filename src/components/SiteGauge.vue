<template>
  <vue-gauge
    :refid="'site-gauge-id'"
    :options="{
      'arcDelimiters': [75],
      'hasNeedle': false,
      'arcColors': ['#00ff00', '#d8d8d8'],
      'arcLabels': ['75%'],
      'rangeLabel': ['0%','100%'],
      'chartWidth': 275,
    }" />
</template>

<script>
import VueGauge from 'vue-gauge';

export default {
  name: 'SiteGauge',
  components: { VueGauge }
}
</script>

<style scoped>

</style>