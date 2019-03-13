<template>
  <div>
    <x-header left-options="{showBack: true}">登录</x-header>
    <group title="用户说明">
    <x-input title="手机号码" mask="999 9999 9999" :max="13" is-type="china-mobile"></x-input>
    <x-input title="密码" mask="99999999999" :max="13" type="password"></x-input>
    </group>
    <div class="btn">
    <x-button @click.native="login">登陆</x-button>
    </div>
  </div>
</template>

<script>
import { Group, Cell, XInput, XButton, XHeader } from 'vux'

export default {
  components: {
    Group,
    Cell,
    XInput,
    XButton,
    XHeader
  },
  name: 'Home',
  methods: {
    login () {
      this.$router.push('/')
    }
  },
  data () {
    return {
      msg: 'Hello World!'
    }
  }
}
</script>

<style>
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
</style>
