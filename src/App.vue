<template>
  <div class="gauges">
    <div><CPUsGauge />CPUs</div>
    <div><PodsGauge />Pods</div>
    <div><ClustersGauge />Clusters</div>
    <div><SiteGauge />Site</div>
  </div>
</template>

<script>
import PodsGauge from './components/PodsGauge.vue';
import CPUsGauge from './components/CPUsGauge.vue';
import ClustersGauge from './components/ClustersGauge.vue';
import SiteGauge from './components/SiteGauge.vue';

export default {
  name: 'App',
  components: {
    PodsGauge,
    CPUsGauge,
    ClustersGauge,
    SiteGauge,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
  font-weight: 800;
}
.gauges {
  background-color: #defeff;
  border-radius: 10px;
  margin: 0 auto;
  padding: 20px 5px;
  width: max-content;
}
.gauges > div {
  display: inline-block;
  width: 25%;
}
</style>
