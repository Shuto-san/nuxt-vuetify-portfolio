<template>
    <div id="history">
        <v-container
        fluid>
            <v-card
            width="100vw"
            >
            <v-card-title
            class="justify-center"
            >
                - History -
            </v-card-title>

              <v-timeline>
                <v-timeline-item
                  v-for="(year, i) in years"
                  :key="i"
                  :color="year.color"
                  small
                >
                  <template v-slot:opposite>
                    <span
                      :class="`title font-weight-bold ${year.color}--text`"
                      v-text="year.year"
                    ></span>
                  </template>
                  <div class="py-4">
                    <h2 :class="`title font-weight-light mb-4 ${year.color}--text`">{{ year.title }}</h2>
                    <div>
                        {{ year.content }}
                    </div>
                  </div>
                </v-timeline-item>
              </v-timeline>
            </v-card>
        </v-container>

    </div>
</template>
<script>
  export default {
    data: () => ({
      years: [
        {
          color: 'cyan',
          year: '2011~2015',
          title: '東北大学',
          content: '体育会サッカー部のガチ勢。引くほどストイックだったらしい'
        },
        {
          color: 'green',
          year: '2015',
          title: 'ドイツ留学',
          content: 'サッカーとヨーロッパ旅行のために1年間留学（は冗談で、普通の交換留学）'
        },
        {
          color: 'pink',
          year: '2015~2018',
          title: '東北大学院電気系',
          content: 'プラズマを研究。学術論文英語で2本執筆。台湾の国際学会で放電シミュレーション研究発表'
        },
        {
          color: 'amber',
          year: '2018',
          title: 'フロントSE',
          content: '某大手SIerで業務システム保守＆開発。Web業界に惹かれて1年で転職'
        },
        {
          color: 'orange',
          year: '2019',
          title: 'Webエンジニア',
          content: '某メガベンチャーでWebアプリ開発（主にLaravel, Vue）。仕事ツラいけどプログラミングは楽しい'
        },
      ],
    }),
  }
</script>
<style>
</style>
