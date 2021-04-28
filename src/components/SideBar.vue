<template>
  <div class="row m-0">
    <div class="col-12 p-0">
      <ul>
        <a href="/" class="px-0 px-md-4 text-center text-md-left py-2 sideLink">
          <li>
            <i class="fas fa-bell"></i>
            <span class="d-none d-md-inline-block ml-2">Alerts</span>
          </li>
        </a>
        <a href="/" class="px-0 px-md-4 text-center text-md-left py-2 sideLink">
          <li>
            <i class="fas fa-book-dead"></i>
            <span class="d-none d-md-inline-block ml-2">Reports</span>
          </li>
        </a>
        <a href="/" class="px-0 px-md-4 text-center text-md-left py-2 sideLink">
          <li>
            <i class="fas fa-calendar-alt"></i>
            <span class="d-none d-md-inline-block ml-2">Calendar</span>
          </li>
        </a>
        <a href="/" class="px-0 px-md-4 text-center text-md-left py-2 sideLink">
          <li>
            <i class="fas fa-cat"></i>
            <span class="d-none d-md-inline-block ml-2">Cats</span>
          </li>
        </a>
        <a href="/" class="px-0 px-md-4 text-center text-md-left py-2 sideLink">
          <li>
            <i class="fas fa-chart-bar"></i>
            <span class="d-none d-md-inline-block ml-2">Charts</span>
          </li>
        </a>
        <a href="/" class="px-0 px-md-4 text-center text-md-left py-2 sideLink">
          <li>
            <i class="fas fa-cocktail"></i>
            <span class="d-none d-md-inline-block ml-2">Cocktails</span>
          </li>
        </a>
        <a href="/" class="px-0 px-md-4 text-center text-md-left py-2 sideLink">
          <li>
            <i class="fas fa-comment"></i>
            <span class="d-none d-md-inline-block ml-2">FAQ</span>
          </li>
        </a>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SideBar',
}
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

.sideLink {
  border-bottom: solid #000 1px;
  color: #fff;
  cursor: pointer;
  display: block;
  font-size: 18px;
  /* padding: 10px 1.5rem; */
}

.sideLink:hover {
  background-color: #00a6ff;
  color: #00ff04;
  text-decoration: none;
  transition-duration: .4s;
}
</style>
