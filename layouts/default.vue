<template>
  <div class="flex-container_Base_A">
    <div class="pagegrid">
      
      <div class="logopurposeback-box" />
      <div class="purposetext-box">
        <Purpose />
      </div>
      <div class="logo-box">
        <img class="logo" src="~assets/graphics/IES_Kids_Logo.svg" />
      </div>
      <div class="nav-box">
        <div class="nav-menu">
          <Nav />
        </div>
      </div>
      <div class="bottom">
        <Hero />
        <Nuxt />
      </div>
    </div>
  </div>
</template>

<style>
@import "~assets/css/stylesheet.css";
.logo {
  width: 60%;
}
.pagegrid {
  width: 100%;
  display: grid;
  grid-gap: 0.5vw;
  grid-template-columns: 5% 20% 2% auto;
  grid-template-rows: auto auto auto auto;
  background-color: rgba(255, 255, 255, 0);
}
.whiteback-box {
  grid-column-start: 1;
  grid-column-end: span 4;
  grid-row-start: 1;
  grid-row-end: span 2;
  background-color: rgba(255, 255, 255, 0);
}
.logo-box {
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: span 2;
  width: 100%;
  height: 100%;
}
.purposetext-box {
  grid-column: 4;
  grid-row: 2;
  display: -webkit-flex;
  display: flex;
  text-align: left;
  line-height: 99%;
  font-size: 3.5vw;
  font-weight: 700;
  color: white;
  height: 8.4vw;
  padding-top: .2vw;
}
.logopurposeback-box {
  grid-row: 2;
  grid-column-start: 1;
  grid-column-end: span 4;
  background-color: rgb(65, 65, 65);
  height: 96%;
  border-radius: 1vw;
  box-shadow: 0.2vw 0.2vw 0.6vw 0.2vw rgba(0, 0, 0, 0.816);
}
.nav-box {
  grid-row: 3;
  grid-column-start: 1;
  grid-column-end: span 4;
  background-color: rgb(65, 65, 65);
  height: 3.4vw;
  border-radius: 1vw;
  box-shadow: 0.2vw 0.2vw 0.6vw 0.2vw rgba(0, 0, 0, 0.816);
  position: -webkit-sticky;
  position: sticky;
  top: 3px;
}
.nav-menu {
  grid-row: 3;
  grid-column-start: 3;
  grid-column-end: span 2;
  height: 3.4vw;
  border-radius: 1vw;
}
.bottom {
  grid-row: 4;
  grid-column: 1 / span 4;
}
</style>
