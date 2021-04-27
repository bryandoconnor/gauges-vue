<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import PodsGauge from './components/gauges/PodsGauge.vue';
import CPUsGauge from './components/gauges/CPUsGauge.vue';
import ClustersGauge from './components/gauges/ClustersGauge.vue';
import SiteGauge from './components/gauges/SiteGauge.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    PodsGauge,
    CPUsGauge,
    ClustersGauge,
    SiteGauge,
    Footer,
  }
}
</script>

<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12 mb-4"><Navbar /></div>
      <div class="col-12 gauges">
        <div class="text-center"><CPUsGauge />CPUs</div>
        <div class="text-center"><PodsGauge />Pods</div>
        <div class="text-center"><ClustersGauge />Clusters</div>
        <div class="text-center"><SiteGauge />Site</div>
      </div>
      <div class="col-12 text-center"><Footer /></div>
    </div>
  </div>
</template>


<style>
a {
  text-decoration: none;
}
body {
  margin: 0;
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
.text-center {
  text-align: center;
}
</style>
