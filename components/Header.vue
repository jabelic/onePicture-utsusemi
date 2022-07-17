<template>
  <v-app-bar :clipped-left="clipped" fixed app>
    <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    <!-- <v-btn icon @click.stop="miniVariant = !miniVariant">
      <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
    </v-btn>
    <v-btn icon @click.stop="clipped = !clipped">
      <v-icon>mdi-application</v-icon>
    </v-btn> -->
    <!-- <v-btn icon @click.stop="fixed = !fixed">
      <v-icon>mdi-minus</v-icon>
    </v-btn> -->
    <!-- <v-toolbar-title v-text="title" /> -->
    <div class="title-box">
      <div class="title">{{ title }}</div>
      <div class="subtitle">{{ subtitle }}</div>
    </div>
    <v-spacer />
    <!-- <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn> -->
  </v-app-bar>
</template>
<script>
import { defineComponent, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const title = ref('絵画工房 サービス名')
    const subtitle = ref('By 絵画工房 空蝉')
    return { title, subtitle }
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
