<template>
	<div class="logo-container">
		<div class="whiteback-box" />
		<div class="logopurposeback-box" />

		<div class="purposetext-box">
			Helping parents raise their kids in Chirst.<br />
			Developing ministers in the Kingdom of God.
		</div>
		<div class="nav-box"></div>
		<div class="nav-menu">
			<Nav />
		</div>
		<div class="logo-box">
			<img class="logo" src="./../assets/graphics/IES_Kids_Logo.svg" />
		</div>
	</div>
</template>
    
<script>
export default {
	name: "logopurpose",
};
</script>

<style>
.logo {
	width: 100%;
}
.logo-container {
	width: 100%;
	display: grid;
	grid-gap: 0.5vw;
	grid-template-columns: 2% 20% 5% auto;
	grid-template-rows: auto auto auto;
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
	grid-row-end: span 3;
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
	padding-top: 1vw;
	padding-bottom: 1vw;
	color: white;
}
.logopurposeback-box {
	grid-row: 2;
	grid-column-start: 1;
	grid-column-end: span 4;
	background-color: rgba(110, 110, 110, 0.7);
	height: 100%;
	border-radius: 1vw;
	box-shadow: 0.2vw 0.2vw 0.6vw 0.2vw rgba(0, 0, 0, 0.816);
}
.nav-box {
	grid-row: 3;
	grid-column-start: 1;
	grid-column-end: span 4;
	background-color: rgb(110, 110, 110, 0.7);
	height: 3.4vw;
	border-radius: 1vw;
	box-shadow: 0.2vw 0.2vw 0.6vw 0.2vw rgba(0, 0, 0, 0.816);
}
.nav-menu {
	grid-row: 3;
	grid-column-start: 3;
	grid-column-end: span 2;
	height: 3.4vw;
	border-radius: 1vw;
}
</style>