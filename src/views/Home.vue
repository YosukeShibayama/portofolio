<template>
  <div>
    <br />
    <Profile />
    <br />

    <v-layout>
      <v-flex xs12 sm6 offset-sm3>
        <v-card>
          <v-tabs v-model="tab" color="" grow>
            <v-tabs-slider color=""></v-tabs-slider>
            <v-tab v-for="item in tabs" :key="item">
              {{ item }}
            </v-tab>
          </v-tabs>

          <v-tabs-items v-model="tab">
            <v-tab-item
              v-for="item in tabs"
              :key="item"
              :transition="false"
              :reverse-transition="false"
            >
              <Portofolio v-if="item === 'Portofolio'" />
              <News v-if="item === 'News'" />
              <Twitter v-if="item === 'Twitter'" />
            </v-tab-item> </v-tabs-items
        ></v-card>
      </v-flex>
    </v-layout>
    <br />
    <Contact />
  </div>
</template>

<script>
import Portofolio from "@/components/Portofolio";
import News from "@/components/News";
import Twitter from "@/components/Twitter";
import Profile from "@/components/Profile";
import Contact from "@/components/Contact";

export default {
  components: { Twitter, News, Portofolio, Profile, Contact },
  data() {
    return {
      tab: null,
      tabs: ["Portofolio", "News", "Twitter"]
    };
  },
  methods: {}
};
</script>
