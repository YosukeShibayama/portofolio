<template>
  <div>
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
        <Contact v-if="item === 'Contact'" />
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
import Portofolio from "@/components/Portofolio";
import News from "@/components/News";
import Contact from "@/components/Contact";

export default {
  components: { Contact, News, Portofolio },
  data() {
    return {
      tab: null,
      tabs: ["Portofolio", "News", "Contact"]
    };
  },
  methods: {}
};
</script>
