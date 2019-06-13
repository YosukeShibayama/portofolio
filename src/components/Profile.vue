<template>
  <v-layout>
    <v-flex xs12 sm6 offset-sm3>
      <v-card>
        <v-img :src="require('../assets/logo.svg')" aspect-ratio="2.75"></v-img>

        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">柴山陽介</h3>
            <div style="white-space:pre-wrap;">
              {{ card_text }}
            </div>
          </div>
        </v-card-title>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      card_text: `2018年3月 慶應義塾大学商学部卒業。医療機器メーカーに就職し、インサイドセールスを経験。
      神社仏閣巡りが趣味。`
    };
  }
};
</script>
