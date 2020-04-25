<template>
    <div id="history">
        <v-container
        fluid>
            <v-card
            width="100vw"
            class="pa-4"
            >
            <v-card-title
            class="justify-center display-1 font-italic"
            >
                History
            </v-card-title>

              <v-timeline style="margin: 0 auto; max-width: 900px">
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
                    <h2 :class="`title font-italic mb-4 ${year.color}--text`">{{ year.title }}</h2>
                    <div v-html="year.content">
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
          year: '2011~15',
          title: '東北大学',
          content: '体育会サッカー部にストイックに打ち込む'
        },
        {
          color: 'green',
          year: '2015~16',
          title: 'ドイツ留学',
          content: 'サッカーとヨーロッパ旅行のために1年間交換留学'
        },
        {
          color: 'pink',
          year: '2015~18',
          title: '東北大学院電気系',
          content: 'プラズマを研究、学術論文英語で2本執筆<br>台湾の国際学会で放電シミュレーション研究発表'
        },
        {
          color: 'amber',
          year: '2018~19',
          title: 'フロントSE',
          content: '某大手SIerで業務システム保守＆開発<br>楽天ハッカソン参加でWeb業界に魅了され1年で転職'
        },
        {
          color: 'orange',
          year: '2019~',
          title: 'Webエンジニア',
          content: '某メガベンチャーでWebアプリ開発(Laravel,Vue,Java)<br>仕事ツラいけどプログラミング楽しい'
        },
      ],
    }),
  }
</script>
<style>
</style>
