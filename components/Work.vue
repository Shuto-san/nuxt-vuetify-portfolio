<template>
    <div id="work">
            <v-container
            fluid>
                <v-card
                width="100vw"
                >
                <v-card-title
                class="justify-center display-1 font-italic"
                >
                    Work
                </v-card-title>
                <v-row
                >
                    <v-col
                      v-for="card in cards"
                      :key="card.title"
                      :cols="card.flex.cols"
                      :sm="card.flex.sm"
                      :md="card.flex.md"
                    >
                    <a :href="card.redirect_url">
                        <v-card>
                          <v-img
                            :src="card.src"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                          >
                            <v-card-title v-text="card.title"></v-card-title>
                            <v-card-text v-text="card.skill"></v-card-text>
                          </v-img>
                        </v-card>
                    </a>
                    </v-col>
                </v-row>
                </v-card>
            </v-container>
    </div>
</template>
<script>
  export default {
    data: () => ({
      cards: [
        { title: 'Portfolio Page', skill: 'Nuxt×Vuetify', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', redirect_url: 'https://shoot-portfolio.netlify.com/' ,flex: {cols: 12, sm: 6, md: 6}},
        { title: 'Twitter-like SNS', skill: 'Laravel×Vue×MySql×MySql×Redis', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', redirect_url: 'https://kumatetsublog.com/laravel-tutorial-web-application' ,flex: {cols: 12, sm: 6, md: 6} },
        { title: 'SHOOT Blog', skill: 'Wordpress', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', redirect_url: 'https://kumatetsublog.com/' ,flex: {cols: 12, sm: 6, md: 6} },
      ],
    }),
  }
</script>
<style>
</style>
