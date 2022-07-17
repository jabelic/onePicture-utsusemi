<template>
  <v-app-bar fixed app>
    <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    <v-avatar class="mr-3" color="grey lighten-5 my-auto" size="60">
      <v-img contain max-height="90%" :src="iconSrc"></v-img>
    </v-avatar>
    <div class="title-box">
      <div class="title">{{ title }}</div>
      <div class="subtitle">{{ subtitle }}</div>
    </div>
    <v-spacer />
  </v-app-bar>
</template>
<script>
import { defineComponent, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const title = ref('絵画工房 サービス名')
    const subtitle = ref('By 絵画工房 空蝉')
    const iconSrc = require('@/assets/image/icon.png')
    const drawer = ref(false)
    return { title, subtitle, iconSrc, drawer }
  },
})
</script>
<style scoped>
.title-box {
  display: flex;
  display: -webkit-flex;
  /* justify-content: space-between; */
  flex-direction: row;
  width: 100vw;
  /* margin-top: auto; */
  /* margin-left: 2%; */
}
.title {
  flex-direction: row;
  margin-bottom: 0.5vh;
}
.subtitle {
  flex-direction: row;
  margin-top: auto;
  margin-left: 2%;
  margin-bottom: 1vh;
}
</style>
