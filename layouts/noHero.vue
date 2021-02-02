<template>
  <div class="flex-container_Base_A">
    <div class="topBar">
      <Nav />
    </div>
    <Nuxt />
  </div>
</template>


<style scoped>
    @import '~assets/css/stylesheet.css';
.topBar {
 overflow: hidden;
 position: fixed;
 top: 0;
 width: 100%; 
 background-color: rgb(46, 46, 46);
}
</style>
