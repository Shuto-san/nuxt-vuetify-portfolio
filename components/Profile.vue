<template>
    <div id="profile">
        <v-container
        fluid>
        <v-card
        width="100vw"
        >
        <v-card-title
        class="pa-5 justify-center display-1 font-italic"
        >
        Profile
    </v-card-title>

    <v-row
    justify="center"
    align-content="center"
    >
    <v-col
    cols="12"
    sm="5"
    md="5"
    align="center"
    >
    <v-row
    justify="space-around"
    align-content="center"
    style="height:100%"
    >
    <v-avatar
    width="80%"
    height="auto"
    >
    <img
    src="/image/my-portfolio-profile.jpg"
    alt="SHOOT"
    style="object-fit: cover;"
    >
</v-avatar>
</v-row>
</v-col>
<v-col
cols="12"
sm="6"
md="6"
>
<v-list>
    <v-list-item
    v-for="profile in profiles"
    :key="profile.content"
    >
    <v-list-item-content>
        <v-list-item-title><v-icon>mdi-check</v-icon> {{ profile.content }}</v-list-item-title>
    </v-list-item-content>
</v-list-item>
</v-list>
</v-col>
</v-row>
</v-card>
</v-container>
</div>
</template>
<script>
export default {
    data: () => ({
        profiles: [
            { content: 'SHOOT（しゅーと）'},
            { content: '1993年かわさき生まれ'},
            { content: 'Webエンジニア×ブロガー'},
            { content: 'プログラミングとブログ好き'},
            { content: 'サッカーとミスチル狂'},
            { content: '嫁大好き'},
            { content: '幼少期ドイツ在住（5年間）'},
            { content: 'マイペースで平和主義'},
            { content: '末っ子×ゆとり'},
            { content: '英語しゃべれる。TOEIC890'},
            { content: '基本情報技術者'},
        ],
    }),
}
</script>
<style>
</style>
