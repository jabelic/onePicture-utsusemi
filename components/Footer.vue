<template>
  <v-footer :absolute="!fixed" app>
    <span>&copy; {{ credit }}</span>
  </v-footer>
</template>
<script>
import { defineComponent, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const fixed = false
    const credit = ref(`Jabelic - ${new Date().getFullYear()}`)
    return { credit, fixed }
  },
})
</script>
