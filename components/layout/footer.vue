<template>
  <div class="footer">
    <div>
      Meta
      基本データ
      ブログ
      求人
      ヘルプ
      API
      プライバシー
      利用規約
      人気アカウント
      ハッシュタグ
      所在地
      Instagram Lite
      日本語
    </div>

    <div>
      日本語
      © 2021 Instagram from Meta
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class Footer extends Vue {
}
</script>

<style lang="scss" scoped>
  .footer{
    position: fixed;
    bottom: 0;
  }
</style>
