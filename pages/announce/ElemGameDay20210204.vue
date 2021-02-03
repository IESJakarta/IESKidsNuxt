<template>
	<div class="flex-container_Base_A">
		<div><p /></div>
		<div class="flex-item_SpText">
			<p>
				<img
					src="~/assets/graphics/AnnounceTemp/ElmGameTime20210204-med.jpg"
					referrerpolicy="no-referrer"
					alt="ElmGameTime20210204"
				/>
			</p>
			<p>
				<center>
					Join our Zoom Game-time for kids ages 6-9, happening on
					<strong>Thursday, 4 February 2021 at 4PM</strong>.
					<div><br /></div>
					We'll have a special game segment led by one of the Kids Church
					teachers, followed by prayer time.
				</center>
			</p>
			<p>
				<center>
					<strong
						>IES Kids Church is inviting you to Elementary Zoom - Game Time
					</strong>
				</center>
			</p>
			<p>Thursday, February 4, 2021 4pm - 4:45pm</p>
		</div>
		<div class="flex-item_SpText">
			<p>
				<center>
					For questions or to get the Zoom link, please <br> 
                    WhatsApp IES Kids from
					<a
						href="https://wa.me/628159460826?text=Hi%20Kristin.%20My%20name%20is%20_________.%20%0D%0AI%27d%20like%20to%20ask%20you%20
                more%20about%20the%20upcoming%20IES%20Kids%20Elementary%20Zoom%20Game%20Time.%20%0D%0AMy%20child%27s%20name%20is%20_______________."
						>here</a> or email Kristin at
					<a href="mailto:kristin@iesjakarta.org">kristin@iesjakarta.org</a>.
				</center>
			</p>
		</div>
	</div>
</template>
<script>
export default {
    layout: "noHero",
    head() {
      return {
        title: this.title,
        meta: [
          // hid is used as unique identifier. Do not use `vmid` for it as it will not work
          {
            'og:description': 'Elementary Game Day 2021 02 04',
            'og:title': 'IES Kids Church',
            'og:url': 'https://ieskids.org/announce/elemgameday20210204/',
            'og:image': 'https://ieskids.org/_nuxt/img/ElmGameTime20210204-med.a0dd5ac.jpg'
          }
        ]
      }
    }
};
</script>
<style>
@import "~assets/css/stylesheet.css";
</style>
