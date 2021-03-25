<template>
	<div style="background-color: #d8dce0">
		<br />

		<div
			class="flex-container__Base_A"
			style="
				flex-direction: column;
				justify-content: center;
				align-items: center;"
		>
			<!-- this div covers us if nothing is going on and there's not data to show. -->
			<div
				v-if="regPageData.length == 0"
				class="flex-container_2A"
				style="text-align: center; background-color: #cee5f1"
			>
				<h2>
					<h2a> IES Kids LG Info & Registration</h2a>
				</h2>
				<div style="text-align: center; width: 80%">
					<p>
						<strong>
							Currently, we have no IES Kids LifeGroups scheduled to open for
							registration.
						</strong>
					</p>
					<p>
						If you have questions, please send us a message through our
						<a
							href="https://wa.me/628159460826?text=Hi%20IES%20Kids.%20My%20name%20is%20_________.%20%0D%0AI%27d%20like%20to%20ask%20you%20
                more%20about%20the%20upcoming%20IES%20Kids%20LG.%20%0D%0AMy%20child%27s%20name%20is%20_______________."
							target="”_blank”"
							>IES Kids WhatsApp number</a
						>
						by cliking the link. If you prefer email, you may email Kristin, our
						IES Kids Ministry Director, at her email address:
						<a href="mailto:kristin@iesjakarta.org"> kristin@iesjakarta.org</a>
					</p>
				</div>
			</div>

			<!-- this div is the main section -->
			<div
				v-else-if="regPageData"
				class="flex-container_2A"
				style="text-align: center; background-color: #cee5f1"
			>
				<h2>
					<h2a> IES Kids LG Info & Registration</h2a>
				</h2>
				<div style="text-align: center; width: 80%">
					<p>
						<strong>
							We have {{ offeredLGCount }} upcoming IES Kids LifeGroup<span
								v-if="offeredLGCount > 1"
								>s
							</span>
							open for registration.<br> Our first meeting for this round starts
							{{ regPageData[0].FirstSessionDate }}!
						</strong>
					</p>

					<div>
						<!-- communication logic in this div -->

						<div v-if="closedRegLGCount == 0 && offeredLGCount == 2">
							Both groups are currently open for registration.
						</div>

						<div v-else-if="closedRegLGCount == 0 && offeredLGCount > 2">
							All groups are currently open for registration.
						</div>
					</div>
					<div>
						<div v-if="closedRegLGCount > 0 && openRegLGCount == 1">
							Registration has already closed for {{ closedRegLGCount }} of our
							LGs,
							<br />
							but there is still {{ openRegLGCount }} LG with open spots.
						</div>
						<div v-else-if="closedRegLGCount > 0 && openRegLGCount > 1">
							Registration has already closed for {{ closedRegLGCount }} of our
							LGs, but there are {{ openRegLGCount }} LGs still open for
							registration.
						</div>
						<!--   -->
					</div>

					<p>
						These LifeGroups will be held on the Zoom platform. Please check the
						individual LG schedules below and choose the group that best suits
						your child’s schedule. Register as soon as possible; groups are
						limited to 12 participants per group.
					</p>

					<div v-if="closedRegLGCount == offeredLGCount">
						<strong
							>Registration for this round of IES Kids LGs is closed.</strong
						>
					</div>
					<!--As groups are filled registration
						will be closed.-->
				</div>
				<div class="grid_Internal">
					<div v-for="link in offeredLGShow" v-bind:key="link.Title">
						<div v-if="link.Show == 'TRUE'" class="grid_Internal">
							<div
								class="flex-item_SpText"
								:style="{ 'background-color': link.BackgroundColor }"
							>
								<div class="grid_Internal">
									<div v-if="link.Open == 'TRUE'">
										<img
											:src="
												require('~/assets/graphics/Kids_LG_Reg/' +
													link.OpenGraphic)
											"
											:alt="link.Title + 'for Kids Every ' + link.MeetingDay"
											width="auto"
											height="250px"
										/>
									</div>
									<div v-else-if="link.Open == 'FALSE'">
										<img
											:src="
												require('~/assets/graphics/Kids_LG_Reg/' +
													link.ClosedGraphic)
											"
											:alt="link.Title + 'for Kids Every ' + link.MeetingDay"
											width="auto"
											height="250px"
										/>
									</div>

									<div>
										<h2>{{ link.Title }}</h2>
										<br />
										<strong>{{ link.MeetingDay }}</strong
										>, {{ link.MeetingTime }}<br />
										<strong>Start Date</strong>: {{ link.FirstSessionDate
										}}<br />
										<strong>End Date</strong>: {{ link.LastSessionDate }}<br />
										<strong>LG Registration Full</strong>
										<!--<a
									href="https://iesjakarta.churchcenter.com/registrations/events/661302&ref=LinkToWisdomLG"
									target="_blank"
									><strong>CLICK HERE TO REGISTER</strong></a
								>-->
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>

				<div class="flex-item_SpText">
					<p>
						For questions, please email Kristin at
						<a href="mailto:kristin@iesjakarta.org">kristin@iesjakarta.org</a>
						or WhatsApp from
						<a
							href="https://wa.me/628159460826?text=Hi%20Kristin.%20My%20name%20is%20_________.%20%0D%0AI%27d%20like%20to%20ask%20you%20
                            more%20about%20the%20upcoming%20IES%20Kids%20LG.%20%0D%0AMy%20child%27s%20name%20is%20_______________."
							target="_blank"
							>here</a
						>.
					</p>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
import axios from "axios";
export default {
	layout: "noHero",

	async asyncData() {
		const regPageData = await fetch(
			"https://api.steinhq.com/v1/storages/5d0374a0e8f87532b83a4e3b/KidsLGRegPage"
		).then((res) => res.json());
		return { regPageData };
	},
	computed: {
		offeredLGCount() {
			return this.regPageData.filter((item) => item.Show == "TRUE").length;
		},
		offeredLGShow() {
			return this.regPageData.filter((item) => item.Show == "TRUE");
		},
		openRegLG() {
			return this.offeredLGShow.filter((item) => item.Open == "TRUE");
		},
		openRegLGCount() {
			return this.openRegLG.length;
		},
		closedRegLG() {
			return this.offeredLGShow.filter((item) => item.Open == "FALSE");
		},
		closedRegLGCount() {
			return this.closedRegLG.length;
		},
	},
};
</script>

<style>

</style>
