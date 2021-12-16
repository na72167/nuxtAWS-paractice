<template>

<div class="login-t">
  <div class="login">
    <div class="login__block-wrap">
      <img class="login__block-logoImg" :src="require('@/assets/img/mainLogo.svg')">

      <div class="login__block-inputWrap">
        <label class="#">
          <span class="login__block-inputFont">
            電話番号、ユーザーネーム、メールアドレス
          </span>
          <input class="login__block-input" placeholder="">
        </label>
      </div>

      <div class="login__block-inputPasswordWrap">
        <label>
          <span class="login__block-inputFont">
            パスワード
          </span>
          <input class="login__block-input">
        </label>
        <div class="login__block-displayButton">
          <span>表示する</span>
        </div>
      </div>

      <div class="login__block-inputPasswordWrap">
        <label>
          <span class="login__block-inputFont">
            確認用パスワード
          </span>
          <input class="login__block-input">
        </label>
        <div class="login__block-displayButton">
          <span>表示する</span>
        </div>
      </div>


      <button class="login__block-login">サインアップ</button>

      <div class="login__block-orWrap">
        <div class="login__block-pseudoElement"></div>
        <div class="login__block-orElement">または</div>
        <div class="login__block-pseudoElement"></div>
      </div>

      <div class="login__block-facebookWrap">
        <icon>f</icon>
        <div class="login__block-facebook">Facebookでログイン</div>
      </div>

      <div class="login__block-forgetPasswordLink">パスワードを忘れた場合</div>

    </div>

  </div>

  <div class="login__acountBlock">
    <span class="login__acountBlock-signUpLink">アカウントをお持ちですか？</span>
    <a class="login__acountBlock-RegistLink" @click="handleLoginComponentsButton()">ログインする</a>
  </div>

  <div>
    <div>
      <span>ダウンロード</span>
    </div>
    <div>
      <img class="#">
      <img class="#">
    </div>
  </div>

</div>


</template>

<script lang="ts">
import { Component,Emit,Vue } from 'vue-property-decorator'
import { SignUpOrLogin } from '@/interfaces/template';

@Component
export default class SignUp extends Vue {

  @Emit()
  public handlelogin(s: SignUpOrLogin) {}

  public handleLoginComponentsButton(): void {
    this.handlelogin('login');
  }

}
</script>

<style lang="scss" scoped>
  .login{
    background: #fff;
    height: 402px;
    width: 350px;
    min-width: 350px;
    border: 1px solid #dbdbdb;
    border-radius: 1px;
    padding: 30px 40px 10px;
    &__block{
      &-inputWrap{
        padding: 0 10px;
        border: 1px solid #dbdbdb;
        border-radius: 2px;
      }
      &-inputFont{
        font-size: 11px;
        color: #dbdbdb;
      }
      &-inputPasswordWrap{
        margin-top: 10px;
        border-radius: 1px;
        padding: 0 0 0 10px;
        border: 1px solid #dbdbdb;
        border-radius: 2px;
        display: flex;
      }
      &-logoImg{
        margin:0 44px 30px;
      }
      &-input{
        font-size:3em;
        width: 160px;
        font-size: 11px;
        padding: 0px 0 0px 2px;
        border: none;
        outline: none;
      }
      &-displayButton{
        font-weight: bold;
        font-size: 14px;
        height: 40px;
        width: 90px;
        background: #fff;
        padding: 10px 0px 10px 10px;
      }
      &-login{
        margin-top: 10px;
        background: #2395F6;
        color: #fff;
        font-weight: bold;
        width: 270px;
        border: none;
        padding: 4px 2px;
        border-radius: 2px;
        outline: none;
      }
    }

    &__acountBlock{
      background: #fff;
      font-weight: solid;
      min-width: 320px;
      padding: 20px 40px;
      margin-top: 12px;
      border: 1px solid #dbdbdb;
      border-radius: 2px;
      font-size: 13px;
      &-RegistLink{
        color: #2395F6;
        font-weight: bold;
      }
    }
  }
</style>
