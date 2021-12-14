<template>
  <div class="default">
    <!-- <Header/> -->
      <client-only>
        <Nuxt/>
      </client-only>
    <!-- <Footer/> -->
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
// import Header from '@/components/layout/header';
// import Footer from '@/components/layout/footer';

@Component
// ({
//   components: {
//     Header,
//     Footer,
//   },
// })
export default class defaultlayout extends Vue {
}
</script>

<style lang="scss" scoped>
</style>

