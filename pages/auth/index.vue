<template>

  <section>
    <div class="wrap">
      <img class="wrap-spImg" :src="require('@/assets/img/spImg.svg')">
      <Login
        v-if="authState === 'login'"
        @handlesignup="changeSignUpComponets"
      />
      <SignUp
        v-if="authState === 'signUp'"
        @handlelogin="changeLoginComponets"
      />
    </div>
  </section>

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { SignUpOrLogin } from '@/interfaces/template';
import Login from '@/components/custom/auth/login.vue';
import SignUp from '@/components/custom/auth/signUp.vue';

@Component({
  components: {
    Login,
    SignUp
  },
})
export default class defaultlayout extends Vue {

  public authState: SignUpOrLogin = 'login';

  public changeSignUpComponets(s: SignUpOrLogin): void {
    this.authState = s;
  }

  public changeLoginComponets(s: SignUpOrLogin): void {
    this.authState = s;
  }

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
