<template>

  <section>
    <div class="wrap">
      <img class="wrap-spImg" :src="require('@/assets/img/spImg.svg')">
      <Login/>
    </div>
  </section>

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Login from '@/components/custom/auth/login.vue';

@Component({
  components: {
    Login
  },
})
export default class defaultlayout extends Vue {
}
</script>

<style lang="scss" scoped>
  .wrap{
    position: relative;
    top: 115px;
    height: 580px;
    min-width: 745px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    &-spImg{
      height: 580px;
      width: 365px;
      margin-right: 30px;
    }
  }
</style>
