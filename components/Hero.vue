<template>
  <div>
    <div class="whitespace" />
    <div class="parallax">
        <div style="height:45vw">
        </div>
    </div>
  </div>
</template>
<style>
.whitespace {
  background-color: white;
  height: 18.5vw;
  border-radius: 15px;
  box-shadow: 2px 2px 6px 0px rgba(0, 0, 0, 0.3);
}
.parallax {
  /* The image used */
  background-image: url('./../assets/graphics/Photos/GroupCityWalkCropNarrow.jpg');


  /* Full height */
  height: 45vw; 

  /* Create the parallax scrolling effect */
  background-attachment: scroll;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 15px;
  box-shadow: 2px 2px 6px 0px rgba(0, 0, 0, 0.3);

}
</style>