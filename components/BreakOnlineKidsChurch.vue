<template>
  <div>
    <div class="flex-container_1" v-for="link in links" v-bind:key="link.BREAK_HTML">
    
        <div v-if="link.BREAK_HTML">
            <p><span style="font-size:80%" v-html="link.BREAK_HTML"></span></p>
        </div>
    
    </div>
  </div>
</template>



<script>
import axios from 'axios';

export default {
    name: 'BreakKidsChurchOnline',
    data () {
        return {
            links: null,
        };
},
created: function() {
    axios
    .get('https://api.steinhq.com/v1/storages/5d0374a0e8f87532b83a4e3b/Break_OnlineKidsChurchLinks')
    .then(res => {
        this.links = res.data;
    })
  }
}
</script>

<style>
    @import './../assets/css/stylesheet.css';
</style>