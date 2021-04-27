<template>
  <div class="row m-0 text-center">
    <div class="col-12 p-0">
      <p class="footer m-0">
        <a href="/" class="footLink">Mechagon © <span>{{(new Date().getFullYear())}}</span></a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  // components: { VueGauge }
  setup() {
    return {
      Quantity: 20
    }
  },
}
</script>

<style scoped>
.footer {
  background-color: #000;
  padding: .625rem;
}

p.footer {
  padding: .625rem;
}

.footLink {
  background-color: #000;
  color: #fff;
  font-size: 20px;
  font-family: 'Helvetica', sans-serif;
}

.footLink:hover {
  color: orange;
  text-decoration: none;
  transition-duration: .8s;
}
</style>