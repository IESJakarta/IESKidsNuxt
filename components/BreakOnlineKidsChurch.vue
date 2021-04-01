<template>
	<div>
		<div
			v-for="link in links"
			v-bind:key="link.SortOrder"
		>
			<div><br /></div>

			<!-- this is the head -->
			<div v-if="link.Category === 'Header Content'">
				<div
					class="flex-container_3A"
					style="text-align: center"
					:style="{ backgroundColor: link.Week_Card_Color }"
				>
					<h2>
						{{ link.SectionTitle }} <br />
						{{ link.Week }}
					</h2>
					<div v-if="link.SectionSubTitle">
						<h3>{{ link.SectionSubTitle }}</h3>
					</div>
					<div v-if="link.Text">
						{{ link.Text }}
					</div>
					<div v-if="link.ifLocalGraphic">
						<div class="flex-item_1">
							<a
								v-bind:href="
									link.Graphic_Link +
									'&ref=Kids_Break_Header_Graphic_Link_' +
									link.SectionTitle
								"
								target="_blank"
							>
								<img
									style="height: auto; max-width: 350px; object-fit: contain"
									:src="require(`../assets/graphics/${ link.ifLocalGraphic }`)"
								/>
							</a>
						</div>
					</div>
					<div v-else-if="link.Graphic">
						<div class="flex-item_1">
							<a
								v-bind:href="
									link.Graphic_Link +
									'&ref=Kids_Break_Header_Graphic_Link_' +
									link.SectionTitle
								"
								target="_blank"
							>
								<img
									style="height: auto; max-width: 350px; object-fit: contain"
									:src="link.Graphic"
								/>
							</a>
						</div>
					</div>
					<div v-if="link.HTMLContent">
						<div class="flex-item_1">
								<span style="font-size: 80%" v-html="link.HTMLContent"></span>
						</div>
					</div>
				</div>
				<div><p /></div>

				<div
					class="flex-container_2A"
					:style="{ backgroundColor: link.Week_Card_Color }"
				>
					<div class="grid_Internal">
						<div v-for="link in links.slice(2)" v-bind:key="link.SortOrder">
							<div v-if="link.Category === 'Section Content'">
								<div
									class="flex-container_3A"
									style="text-align: center"
									:style="{ backgroundColor: link.Curriculum_level_box_Color }"
								>
                                    <div class="flex-item_1">

									<h2>
										{{ link.SectionTitle }}									</h2>
									<div v-if="link.SectionSubTitle">
										<h3>{{ link.SectionSubTitle }}</h3>
									</div>
                                    </div>
									<div v-if="link.Text" class="flex-item_2">
										{{ link.Text }}
									</div>

									<div v-if="link.ifLocalGraphic">
										<div class="flex-item_1">
											<a
												v-bind:href="
													link.Graphic_Link +
													'&ref=Kids_Break_Header_Graphic_Link_' +
													link.SectionTitle
												"
												target="_blank"
											>
												<img
													style="height: auto; width: 100%; object-fit: contain"
													:src="require(`../assets/graphics/${ link.ifLocalGraphic }`)"
												/>
											</a>
										</div>
									</div>

									<div v-else-if="link.Graphic">
										<div class="flex-item_1">
											<a
												v-bind:href="
													link.Graphic_Link +
													'&ref=Kids_Break_Header_Graphic_Link_' +
													link.SectionTitle
												"
												target="_blank"
											>
												<img
													style="height: auto; width: 100%; object-fit: contain"
													:src="link.Graphic"
												/>
											</a>
										</div>
									</div>
									<div v-if="link.HTMLContent">
										<div class="flex-item_2">
												<span
													style="font-size: 80%"
													v-html="link.HTMLContent"
												></span>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>



<script>
import axios from "axios";

export default {
	name: "BreakKidsChurchOnline",
	data() {
		return {
			links: null,
		};
	},
	created: function () {
		axios
			.get(
				"https://api.steinhq.com/v1/storages/5d0374a0e8f87532b83a4e3b/Break_OnlineKidsChurchLinks"
			)
			.then((res) => {
				this.links = res.data;
			});
	},
};
</script>

<style>
    @import '~assets/css/stylesheet.css';
</style>
