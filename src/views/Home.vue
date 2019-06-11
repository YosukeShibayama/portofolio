<template>
  <div>
    <v-tabs v-model="tab" color="" grow>
      <v-tabs-slider color=""></v-tabs-slider>
      <v-tab v-for="item in 3" :key="item">
        {{ item }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="item in 3"
        :key="item"
        :transition="false"
        :reverse-transition="false"
      >
        <HelloWorld v-if="item === 1" />
        <HelloWorld v-if="item === 2" />
        <HelloWorld v-if="item === 3" />
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";

export default {
  components: { HelloWorld },
  data() {
    return {
      tab: null
    };
  },
  methods: {}
};
</script>
