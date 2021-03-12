<template>
  <v-app>
  <v-toolbar
    dark
    height="150px"
    max-height="150px"
    src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAANwAAADcCAMAAAAshD+zAAAAA1BMVEX+qlQgzqKOAAAARklEQVR4nO3BMQEAAADCoPVPbQsvoAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA/ga97AABJRXjUgAAAABJRU5ErkJggg=="
    class="clipheader"
    >
    <!-- これで、斜めに画像をカットすることが出来る
    :style="'clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%))'"
    :style="'clip-path: polygon(左上（X,Y座標）0 0, 右上（X,Y座標）100% 25%, 右下（X,Y座標）100% 100%, 左下（X,Y座標）0 100%)'" -->
    <v-toolbar-title>
        <v-img
        max-height="50"
       max-width="50"
       >
      <!-- 相対パスでやる場合は、:src="require('/header.png')"で表記する必要がある -->
      </v-img>
      </v-toolbar-title>
        <router-link to="/"><v-img
        max-height="50"
       max-width="50"
       :src="require('@/assets/home.svg')"
       >
      <!-- 相対パスでやる場合は、:src="require('/header.png')"で表記する必要がある -->
      </v-img></router-link>
        <router-link to="/serves">サービス</router-link>
        <router-link to="/company">事業概要</router-link>
        <router-link to="/contactUs">お問い合わせ</router-link>
    </v-toolbar>
    
  <router-view />
  
  </v-app>
</template>

<script>

export default {
  name: 'App',
  components:{

  },
};
</script>
<style>
.clipheader{
  z-index:10;
  clip-path: polygon(0 0,80% 0, 90% 0, 0 100%);
}
.clipmain{
  z-index:3;
  position:absolete;
  top:-150px;
  transform: skewY(-5deg);
  /* transform: rotate(-5deg); */
  clip-path: polygon(0 0,100% -10%,100% 110%, 0 100%);
}
.clipfooter{
  position:absolete;
  top:-150px;
  transform: skewY(-5deg);
  clip-path: polygon(0 0,100% 0, 100% 50%, 0 100%);
  /*これは斜めにする⇨ transform: rotate(-8deg); */
  /* clip-path: polygon(0 0,100% 0, 100% 50%, 0 100%); */
}
.footerdiv{
padding-left:100px;
}

</style>