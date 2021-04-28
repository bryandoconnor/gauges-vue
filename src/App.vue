<script>
import Navbar from './components/Navbar.vue';
import SideBar from './components/SideBar.vue';
import Footer from './components/Footer.vue';
import PodsGauge from './components/gauges/PodsGauge.vue';
import CPUsGauge from './components/gauges/CPUsGauge.vue';
import ClustersGauge from './components/gauges/ClustersGauge.vue';
import SiteGauge from './components/gauges/SiteGauge.vue';
import BarChart from './components/charts/BarChart.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    SideBar,
    PodsGauge,
    CPUsGauge,
    ClustersGauge,
    SiteGauge,
    BarChart,
    Footer,
  },
  data() {
    return {
      barChartData1: [0, 90, 15, 55, 5, 20, 80, 60, 5, 70, 20, 100],
      barChartData2: [10, 40, 10, 100, 30, 20, 40, 70, 55, 25, 35, 10],
    };
  },
}
</script>

<template>
  <div class="container-fluid p-0">
    <div class="row m-0">
      <div class="col-12 p-0">
        <Navbar />
      </div>
    </div>

    <div class="row m-0">
      <div class="col-2 col-md-3 p-0 sidebar-bg">
        <SideBar />
      </div>

      <div class="col-10 col-md-9 px-5 py-4">

        <div class="row py-3 px-0 px-sm-3 gauges-bg br-10">
          <div class="col-12 col-lg-6 p-0">
            <div class="row m-0">
              <div class="col-12 text-center"><CPUsGauge /></div>
              <div class="col-12 text-center">CPUs</div>
            </div>
          </div>
          <div class="col-12 col-lg-6 p-0">
            <div class="row m-0">
              <div class="col-12 text-center"><PodsGauge /></div>
              <div class="col-12 text-center">Pods</div>
            </div>
          </div>
          <div class="col-12 col-lg-6 p-0">
            <div class="row m-0">
              <div class="col-12 text-center"><ClustersGauge /></div>
              <div class="col-12 text-center">Clusters</div>
            </div>
          </div>
          <div class="col-12 col-lg-6 p-0">
            <div class="row m-0">
              <div class="col-12 text-center"><SiteGauge /></div>
              <div class="col-12 text-center">Site</div>
            </div>
          </div>
        </div>

        <div class="row py-3 px-0 px-sm-3 my-3 charts-bg br-10">
          <div class="col-12 col-lg-6 my-1 py-3 px-4">
            <div class="row m-0">
              <div class="col-12"><BarChart :data="barChartData1" /></div>
              <div class="col-12 mt-4 text-center">January</div>
            </div>
          </div>
          <div class="col-12 col-lg-6 my-1 py-3 px-4">
            <div class="row m-0">
              <div class="col-12"><BarChart :data="barChartData2" /></div>
              <div class="col-12 mt-4 text-center">February</div>
            </div>
          </div>
        </div>

      </div>
    </div>

    <div class="row m-0">
      <div class="col-12 text-center">
        <Footer />
      </div>
    </div>

  </div>
</template>


<style>
a {
  font-family: 'Share Tech', sans-serif;
  text-decoration: none;
}

body {
  margin: 0;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

.br-10 {
  border-radius: 10px;
}

.charts-bg {
  background-color: #fc6bff;
}

.gauges-bg {
  background-color: #00a6ff;
}

.sidebar-bg {
  background-color: #888;
}
</style>
