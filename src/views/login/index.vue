<template>
  <div class="login-wrap">
    <van-nav-bar title="登录" />
    <form>
      <van-cell-group>
        <van-field v-model="user.mobile"
                   clearable
                   left-icon="manager"
                   label="手机号"
                   placeholder="请输入手机号" />
        <van-field v-model="user.code"
                   center
                   clearable
                   left-icon="eye"
                   label="验证码"
                   placeholder="请输入验证码">
          <van-button slot="button"
                      size="small"
                      type="primary">发送验证码</van-button>
        </van-field>
      </van-cell-group>
      <div class="login-btn">
        <van-button class="btn"
                    type="info"
                    @click.prevent="handleLogin">登录</van-button>
      </div>
    </form>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'LoginIndex',
  data () {
    return {
      user: {
        mobile: '',
        code: ''
      }
    }
  },
  methods: {
    async handleLogin () {
      console.log('123')
      const res = await axios({
        method: 'POST',
        url: 'http://toutiao.course.itcast.cn/app/v1_0/authorizations',
        data: this.user
      })
      console.log(res)
    }
  },
  components: {
  }
}
</script>

<style lang="less" scoped>
.login-btn {
  margin-top: 10px;
  padding: 10px;
  .btn {
    width: 100%;
    font-size: 16px;
    border-radius: 5px;
  }
}
</style>
