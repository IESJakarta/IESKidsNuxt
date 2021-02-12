<template>
<div class="flex-container__Base_A" id="SpAnnounce" >
            <div v-for="announce in announcements"  v-bind:key="announce.Special_Announcement_Title">
                <div v-if="announce.Page_on_which_to_show___Home_Page_ === 'Top' ">
                    <div class="flex-container_2A" :style="{ 'backgroundColor': announce.Card_Color }">
                        <div class="grid_Internal">
                            <div class="flex-item_SpText" :style="{ 'backgroundColor': announce.Box_Color }">
                                <h2>
                                    <h2a :style="{ 'color': announce.Title_Font_Color }">
                                        {{ announce.Special_Announcement_Title }}</h2a>
                                </h2>
                                <div style="text-align:center"><span v-html="announce.Special_Announcement_Text"></span>
                                </div>
                                <div v-if="announce.Special_Announcement_Link"><br>
                                    <a v-bind:href="announce.Special_Announcement_Link"
                                        target="_blank">{{ announce.Special_Announcement_Title }} </a>
                                </div>
                            </div>
                            <div class="flex-item_SpItems" :style="{ 'backgroundColor': announce.Box_Color }"
                                v-if="announce.SpAn_LocalGraphicLink">
                                <a v-bind:href="announce.Special_Announcement_Link" target="_blank">
                                    <img style='height: 100%; width: 100%; object-fit: contain'
                                        :src="require(`~/assets/graphics/${ announce.SpAn_LocalGraphicLink}`)">
                                </a>
                            </div>
                            <div class="flex-item_SpItems" :style="{ 'backgroundColor': announce.Box_Color }"
                                v-else-if="announce.Special_Announcement_Graphic_Link">
                                <a v-bind:href="announce.Special_Announcement_Link" target="_blank">
                                    <img style='height: 100%; width: 100%; object-fit: contain'
                                        :src="announce.Special_Announcement_Graphic_Link">
                                </a>
                            </div>
                        </div>
                    </div>
                    <br>
                </div>
            </div>
    </div>
</template>

<script>
export default {
    name: 'AnBottom',
    data () {
        return {
            announcements: []
        }
},
async fetch() {
    this.announcements = await fetch(
        'https://api.steinhq.com/v1/storages/5d0374a0e8f87532b83a4e3b/TestSpAnnouncement_Output'
        ).then(res => res.json())
  }
}
</script>

<style>
    @import '~assets/css/stylesheet.css';
</style>