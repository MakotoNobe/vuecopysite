<template>
    <div class="home">
    <v-img
      height="480px"
      max-width="100%"
      src="https://pbs.twimg.com/profile_banners/877173803108913152/1587195017/1500x500" 
      class="clipmain"
      >
      <!-- max-height="600"
         相対パスでやる場合は、:src="require('/header.png')"で表記する必要がある -->
      </v-img>
       <top/>
        <v-toolbar
          dark
          height="150px"
          max-height="150px"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAANwAAADcCAMAAAAshD+zAAAAA1BMVEX+qlQgzqKOAAAARklEQVR4nO3BMQEAAADCoPVPbQsvoAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA/ga97AABJRXjUgAAAABJRU5ErkJggg=="
          class="clipfooter"
        >
        <div
          class="footerdiv"
        >
        <h2>下克上エンジニア</h2>
        <h1>Sベン</h1>
        </div>
     </v-toolbar>      
    </div>
</template>

<script>
export default {
    name: 'Home',
    components: {},
    methods: {
        switchCreateTaskDialog(value) {
            this.$store.dispatch("switchCreateTaskDialog", value);
        },
        toEventPage(value) {
            this.$router.push(`/event/${value.event.eventNo}`);
        },
    }
};
</script>
