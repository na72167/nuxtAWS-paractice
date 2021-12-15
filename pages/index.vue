<template>
  <div>
    <Auth/>
    <!-- <Home> -->
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Auth from '@/pages/auth/index.vue';

@Component({
  layout: "topPage",
  components: {
    Auth
  }
})
export default class home extends Vue {}
</script>

<style lang="scss" scoped>
</style>
