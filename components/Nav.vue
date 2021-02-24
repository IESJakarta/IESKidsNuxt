<template>
  <nav class="nav">
    <div class="nav__link">
      <nuxt-link to="/">Home</nuxt-link>
    </div>

    <div class="nav__link">
      <nuxt-link to="/Kids Church Online">KidsChurchOnline</nuxt-link>
    </div>

    <div class="nav__link">
      <a href="https://www.iesjakarta.org">IES Jakarta</a>
    </div>

      <div class="l1">
      <a
        href="https://wa.me/6281949668498?text=Hi%20my%20name%20is%20_______.%20I%20got%20your%20number%20from%20the%20IES%20Kids%20web%20page."
        target="_blank"
      >
        <img
          class="littleLogos"
          src="~assets/graphics/ExternalLogos/WhatsAppLogo_Smallest.svg"
        />
      </a>
      </div>

      <div class="l2">
      <a href="https://www.facebook.com/IESKidsChurch/" target="_blank">
        <img
          class="littleLogos"
          src="~assets/graphics/ExternalLogos/Facebook_f_logo_2019_Smallest.svg"
        />
      </a>
      </div>

      <div class="l3">
      <a href="https://www.instagram.com/ieskidschurch/" target="_blank">
        <img
          class="littleLogos"
          src="~assets/graphics/ExternalLogos/Instagram_logo_2016_Smallest.svg"
        />
      </a>
      </div>

      <div class="l4">
      <a href="https://www.youtube.com/IESKidsChurch" target="_blank">
        <img
          class="littleLogos"
          src="~assets/graphics/ExternalLogos/YouTube_social_white_square_2017_Smallest.svg"
        />
      </a>
      </div>

  </nav>
</template>
<script>
export default {};
</script>
<style scoped>
.nav {
  display: grid;
  grid-template-columns: repeat(9, 1fr);
  height: 3vw;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 0.25vw;
}
.nav__link {
  grid-column: 1;
  width: auto;
  display: flex;
  align-items: center;
  border-radius: 4px;
  justify-content: space-around;
  height: 2.3vw;
  font-size: 2.5vw;
  border: 1px solid (110, 110, 110, 0.7);
  background-color: (110, 110, 110, 0.7);
  cursor: pointer;
  padding: 1vw;
}
.nav__link:visited {
  color: white;
}
.nav__link:hover {
  background-color: #acacacbb;
  border: 1px solid #acacacbb;
  color: skyblue;
  box-shadow: 5px 3px 5px 2px #3f41468c;
}
.nuxt-link-exact-active {
  color: skyblue;
}
a {
  color: white;
}
a:visited {
  color: white;
}
a:hover {
  color: skyblue;
}

.littleLogos {
  height: 2.8vw;
  padding: calc(.5vh - .1vw);
}
.smalllogos {
  grid-column: 2 / span 2;
  justify-content: space-around;
  padding-bottom: 1vh;
  grid-template-columns: repeat(4, 1fr);
}
.l1 {
  grid-column: col 1;
}
.l2 {
  grid-column: col 2;
}
.l3 {
  grid-column: col 3;
}
.l4 {
  grid-column: col 4;
}
.l5 {
  grid-column: col 5;
}
.l6 {
  grid-column: col 6;
}
.l7 {
  grid-column: col 7;
}
.l8 {
  grid-column: col 8;
}
.l9 {
  grid-column: col 9;
}
</style>
<style>
@import "./../assets/css/stylesheet.css";
</style>
