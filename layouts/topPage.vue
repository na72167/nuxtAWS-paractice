<template>
  <div class="topPage">
      <client-only>
        <Nuxt/>
      </client-only>
    <Footer/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Footer from '@/components/layout/footer';

@Component({
  components: {
    Footer,
  },
})
export default class topPage extends Vue {
}
</script>

<style lang="scss" scoped>
  .topPage{
    height: 100vh;
    background: #FAFAFA;
  }
</style>

