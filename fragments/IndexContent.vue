<template>
  <div class="index-content">
    <!-- カルーセル -->
    <v-carousel continuous cycle>
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        transition="fade-transition"
        reverse-transition="fade-transition"
      >
        <v-row class="fill-height" align="center" justify="center">
          <img :src="item.src" style="width: auto; height: 100%" />
          <!-- <div class="text-h2">Slide {{ i + 1 }}</div> -->
        </v-row>
      </v-carousel-item>
    </v-carousel>

    <div class="title-label my-10">
      <div>{{ title }}</div>
    </div>

    <br />
  </div>
</template>
<script>
import { defineComponent, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const items = ref([
      { src: require('@/assets/image/pinkGirl.jpeg') },
      { src: require('@/assets/image/seaGirl.jpeg') },
      { src: require('@/assets/image/Top.png') },
    ])
    const title = ref('一覧(title)')
    return { items, title }
  },
})
</script>
<style scoped>
.index-content {
  width: 100vw;
}
.fill-height {
  transition-delay: 100ms;
}
.title-label {
  background-color: white;
  width: 100vw;
  height: 1vh;
  display: flex;
  justify-content: center;
  align-content: center;
}
</style>
