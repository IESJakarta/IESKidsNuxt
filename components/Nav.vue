<template>
    <nav class="nav">
      <div class="nav__link">
        <nuxt-link to="/">Home</nuxt-link>
      </div>
      <div class="nav__link">
        <nuxt-link to="/KidsChurchOnline">Kids Church Online</nuxt-link>
      </div>
      <div class="nav__link">
        <a href="https://www.youtube.com/IESKidsChurch" target="_blank">IES Kids YouTube</a>
      </div>
            <div class="nav__link">
        <a href="https://www.iesjakarta.org">IES Jakarta</a>
      </div>
    </nav>
</template>
<script>
export default {
};
</script>
<style>
    @import './../assets/css/stylesheet.css';
.nav {
    width: 100%;
    height: 3vw;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: .25vw;
}
.nav__link {
    width: 20%;
    display: flex;
    align-items: center;
    border-radius: 4px;
    justify-content: space-around;
    height: 2.3vw;
    font-size: 1.8vw;
    border: 1px solid (110, 110, 110, 0.7);
    background-color: (110, 110, 110, 0.7);
    cursor: pointer;
    padding-bottom: .5vw;
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
</style>