<template>
  <div>
    <x-header :left-options="{showBack: true}">登录</x-header>
    <group title="用户说明">
    <x-input title="手机号码" mask="999 9999 9999" :max="13" is-type="china-mobile" v-model="phone"></x-input>
    <x-input title="密码" mask="99999999999" :max="13" v-model="password" type="password"></x-input>
    </group>
    <div class="btn">
    <x-button @click.native="login">登陆</x-button>
    </div>
  </div>
</template>

<script>
import { Group, Cell, XInput, XButton, XHeader, Alert, AlertModule } from 'vux'

export default {
  components: {
    Group,
    Cell,
    XInput,
    XButton,
    XHeader,
    Alert
  },
  methods: {
    login () {
      if (this.password === '123456') {
        this.$router.push('/')
      } else {
        AlertModule.show({
          title: '登录失败',
          content: '密码错误'
        })
      }
    }
  },
  data () {
    return {
      msg: 'Hello World!',
      phone: '13995953370',
      password: ''
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
