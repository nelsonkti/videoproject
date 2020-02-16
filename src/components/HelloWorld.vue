<template>
  <div class="hello">
    <d-player ref="player" @play="play" :logo="logo" :lang="lang" :video="video" :contextmenu="contextmenu"></d-player>
  </div>
</template>

<script>
import VueDPlayer from './VueDPlayerHls'
import logoImg from '@/assets/logo.png'
export default {
  name: 'HelloWorld',
  data () {
    return {
      video: {
        quality: [{
          name: '清晰',
          url: 'http://ugcsochy.tcdn.qq.com/vwecam.gtimg.com/1006_7087652891204a21af780b7276b1dbbb.f0.mp4?vkey=CE1E19961B48811B65F97C467BBC080CCFC24D0281F01A926D9565206868E0212F5FE96391F9ABF1C7B7E65A3350C71FBDB83A4F0F1A5E29'
        },
        {
          name: '高清',
          url: 'http://ugcsochy.tcdn.qq.com/vwecam.gtimg.com/1006_7087652891204a21af780b7276b1dbbb.f0.mp4?vkey=CE1E19961B48811B65F97C467BBC080CCFC24D0281F01A926D9565206868E0212F5FE96391F9ABF1C7B7E65A3350C71FBDB83A4F0F1A5E29'
        },
        {
          name: '超高清',
          url: 'http://ugcsochy.tcdn.qq.com/vwecam.gtimg.com/1006_7087652891204a21af780b7276b1dbbb.f0.mp4?vkey=CE1E19961B48811B65F97C467BBC080CCFC24D0281F01A926D9565206868E0212F5FE96391F9ABF1C7B7E65A3350C71FBDB83A4F0F1A5E29'
        }],
        pic: '',
        defaultQuality: 1,
        thumbnails: logoImg,
        type: 'auto'
      },
      lang: 'zh-cn',
      logo: logoImg,
      autoplay: false,
      player: null,
      contextmenu: [
      ]
    }
  },
  components: {
    'd-player': VueDPlayer
  },
  methods: {
    play () {
      console.log('开始播放...')
    }
  },
  mounted () {
  // this.player = this.$refs.player.dp;
  // console.log(this.player);
  // var hls = new Hls();
  // hls.loadSource('https://video-dev.github.io/streams/x36xhzz/x36xhzz.m3u8');
  // hls.attachMedia(this.player);
  }
}
</script>

<style scoped>
h1, h2 {
font-weight: normal;
}
ul {
list-style-type: none;
padding: 0;
}
li {
display: inline-block;
margin: 0 10px;
}
a {
color: #42b983;
}
.hello{
  width: 750px;
  margin: 0 auto 50px;
}
@media only screen and (max-width: 640px){
.hello{
    width: 100%;
}
}
</style>
