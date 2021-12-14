<template>

  <section>
    <img :src="require('@/assets/img/spImg.svg')">
    <div>

      <div>
        <img>
        <input>
        <input>
        <button>ログイン</button>

        <div>
          <div></div>
          <div>または</div>
          <div></div>
        </div>

        <div>
          <icon></icon>
          <div>Facebookでログイン</div>
        </div>

        <div>パスワードを忘れた場合</div>
      </div>

      <div>
        <span>アカウントをお持ちでないですか？</span>
        <button>登録する</button>
      </div>

    </div>
  </section>

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  layout: "topPage",
})
export default class defaultlayout extends Vue {
}
</script>

<style lang="scss" scoped>
</style>
