<template>
<div>
            <div class="flex-container_1" v-for="link in links" v-bind:key="link.Week">

                <div class="flex-container_2A" style="text-align: center"
                    :style="{ 'backgroundColor': link.Week_Card_Color }">
                    <h2>
                        <h2a :style="{ 'color': link.Title_Font_Color }">IES Kids Church <br>
                            Online Video Links & Parent Resources<br>
                            {{ link.Week }}
                            </h2a>
                    </h2>
                </div>
                <div><br></div>
                <div class="flex-container_2A" :style="{ 'backgroundColor': link.Week_Card_Color }">
                    <div class="grid_Internal">

                        <div class="flex-container_3A" :style="{ 'backgroundColor': link.Curriculum_level_box_Color }">

                            <div class="flex-item_1">
                                <h2>
                                    <h2a :style="{ 'color': link.Title_Font_Color }">Early Years,<br>
                                        <span style="font-size: 50%">For kids 5 & Under. </span></h2a>
                                </h2>
                            </div>

                            <div class="flex-item_1">
                                <a v-bind:href="link.EarlyYears_Video_Link + '&ref=EarlyYears_Video_Link_' + link.Week"
                                    target="_blank">
                                    <img style='height: auto; width: 100%; object-fit: contain'
                                        :src="link.EarlyYears_Video_Thumbnail">
                                </a>
                            </div>

                            <div class="flex-item_2">
                                <div class="flex-item_L">
                                <h4>
                                    <h2a :style="{ 'color': link.Title_Font_Color }">{{ link.Week }}</h2a>
                                </h4>
                                <a v-bind:href="link.EarlyYears_Video_Link + '&ref=EarlyYears_Video_Link_' + link.Week"
                                    target="_blank">Online Kids Church Video</a>
                                <p style="font-size:80%">{{ link.EarlyYears_Text }}</p>
                                </div>



                                <div v-if="link.EarlyYears_ParentLink">
                                    <h4>
                                        <h2a :style="{ 'color': link.Title_Font_Color }">Parent Resources</h2a>
                                    </h4>

                                    <p style="font-size:80%">We hope you'll sit and watch with your kids, then can carry
                                        on
                                        the discussion through the week. You'll find links below to help you do that and
                                        to help
                                        with your sanity while everyone's home all day long.</p>
                                    <a v-bind:href="link.EarlyYears_ParentLink + '&ref=EarlyYears_ParentLink_' + link.Week"
                                        target="_blank">
                                        Parent's Lesson Extension Link</a>
                                    <br>
                                </div>

                                <div v-if="link.EarlyYears_MusicLinks">
                                    <p style="font-size:80%">Why not get down with your kids and do a little worship.
                                        This is a link
                                        to our regular IES Kids Early Years worship songs.</p>
                                    <p><a v-bind:href="link.EarlyYears_MusicLinks + '&ref=EarlyYears_MusicLinks_' + link.Week"
                                        target="_blank">
                                        Music Resources</a></p>
                                </div>

                                <div v-if="link.EarlyYears_ResourcesHTML">
                                    <p style="line-height:100%">Some EarlyYears resources for
                                        while you're at home</p>
                                    <p><span style="font-size:80%" v-html="link.EarlyYears_ResourcesHTML"></span></p>
                                </div>
                            </div>
                        </div>

                        <div class="flex-container_3A" :style="{ 'backgroundColor': link.Curriculum_level_box_Color }">
                            <div class="flex-item_1">
                                <h2>
                                    <h2a :style="{ 'color': link.Title_Font_Color }">Elementary Years,<br>
                                        <span style="font-size: 50%">For kids 6 to 10 years of age. </span></h2a>
                                </h2>
                            </div>
                            <div class="flex-item_1">
                                <a v-bind:href="link.ElementaryYears_Video_Link + '&ref=ElementaryYears_Video_Link_' + link.Week"
                                    target="_blank">
                                    <img style='height: auto; width: 100%; object-fit: contain'
                                        :src="link.ElementaryYears_Video_Thumbnail">
                                </a>
                            </div>
                            <div class="flex-item_2">
                                <h4>
                                    <h2a :style="{ 'color': link.Title_Font_Color }">{{ link.Week }}</h2a>
                                </h4>
                                <a v-bind:href="link.ElementaryYears_Video_Link + '&ref=ElementaryYears_Video_Link_' + link.Week"
                                    target="_blank">Online Kids Church Video</a>
                                <p style="font-size:80%">{{ link.ElementaryYears_Text }}</p>


                                <div v-if="link.ElementaryYears_ParentLink">
                                    <h4>
                                        <h2a :style="{ 'color': link.Title_Font_Color }">Parent Resources</h2a>
                                    </h4>

                                    <p style="font-size:80%">We hope you'll sit and watch with your kids, then can carry
                                        on
                                        the discussion through the week. You'll find links below to help you do that and
                                        to help
                                        with your sanity while everyone's home all day long.</p>
                                    <a v-bind:href="link.ElementaryYears_ParentLink + '&ref=ElementaryYears_ParentLink_' + link.Week"
                                        target="_blank">
                                        Parent's Lesson Extension Link</a>
                                    <br>
                                </div>

                                <div v-if="link.ElementaryYears_MusicLinks">
                                    <p style="font-size:80%">Why not get down with your kids and do a little worship.
                                        This is a link
                                        to our regular IES Kids Elementary Years worship songs.</p>
                                    <p><a v-bind:href="link.ElementaryYears_MusicLinks + '&ref=ElementaryYears_MusicLinks_' + link.Week"
                                            target="_blank">
                                            Music Resources</a></p>
                                </div>

                                <div v-if="link.ElementaryYears_ResourcesHTML">
                                    <p style="line-height:100%">Some Elementary Years resources for
                                        while you're at home<br>
                                    </p>
                                    <p><span style="font-size:80%" v-html="link.ElementaryYears_ResourcesHTML">
                                        </span>
                                    </p>
                                </div>
                            </div>
                            <br>
                            <br>
                        </div>


                        <div class="flex-container_3A" :style="{ 'backgroundColor': link.Curriculum_level_box_Color }">
                            <div class="flex-item_1">
                                <h2>
                                    <h2a :style="{ 'color': link.Title_Font_Color }">PreTeens,<br>
                                        <span style="font-size: 50%">For our kids 10 to 12 years old. </span></h2a>
                                </h2>
                            </div>


                            <div class="flex-item_2">
                                <div v-if="link.PreTeensZoomDetails">
                                    <div v-html="link.PreTeensZoomDetails"></div>
                                </div>

                                <h4>
                                    <h2a :style="{ 'color': link.Title_Font_Color }">{{ link.Week }}</h2a>
                                </h4>


                                <p style="font-size:80%">{{ link.PreTeens_Text }}</p>

                                <div v-if="link.PreTeens_ParentLink">
                                    <h4>
                                        <h2a :style="{ 'color': link.Title_Font_Color }">Parent Resources</h2a>
                                    </h4>

                                    <p style="font-size:80%">We hope you'll sit and watch with your kids, then can carry
                                        on
                                        the discussion through the week. You'll find links below to help you do that and
                                        to help
                                        with your sanity while everyone's home all day long.</p>
                                    <a v-bind:href="link.PreTeens_ParentLink" target="_blank">
                                        Parent's Lesson Extension Link</a>
                                    <br>
                                </div>

                                <div v-if="link.PreTeens_MusicLinks">
                                    <p style="font-size:80%">Why not get down with your kids and do a little worship.
                                        This is a link
                                        to our regular IES Kids worship songs.</p>
                                    <p><a v-bind:href="link.PreTeens_MusicLinks" target="_blank">
                                            Music Resources</a></p>
                                </div>

                                <div v-if="link.PreTeens_ResourcesHTML">
                                    <p style="line-height:100%">Some PreTeens resources for
                                        while you're at home<br></p>
                                    <p><span style="font-size:80%" v-html="link.PreTeens_ResourcesHTML"></span></p>
                                </div>
                                <br>
                                <br>
                            </div>
                        </div>

                    </div>

                </div>
              <div><br><br></div>
            </div>
</div>            
</template>

<script>
import axios from 'axios';

export default {
    name: 'KidsChurchOnline',
    data () {
        return {
            links: null,
        };
},
created: function() {
    axios
    .get('https://api.steinhq.com/v1/storages/5d0374a0e8f87532b83a4e3b/Test_OnlineKidsChurchLinks')
    .then(res => {
        this.links = res.data;
    })
  }
}
</script>

<style>
    @import '~assets/css/stylesheet.css';

</style>