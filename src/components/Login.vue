<template>
  <div class="container">
    <div class="login_box">
      <!-- 头像 -->
      <div class="avatar_box">
        <img src="../assets/image/img.jpg" alt />
      </div>
      <!-- 登录表单 -->
      <el-form
        :model="loginForm"
        :rules="rules"
        ref="loginForm"
        label-width="0px"
        class="login_form"
      >
        <el-form-item prop="username">
          <el-input v-model="loginForm.username" prefix-icon="iconfont icon-user"></el-input>
        </el-form-item>
        <el-form-item prop="password">
          <el-input v-model="loginForm.password" prefix-icon="iconfont icon-mima"></el-input>
        </el-form-item>
        <el-form-item class="btns">
          <el-button type="primary">登录</el-button>
          <a href="#" style="font-size:12px;padding-left:10px">忘记密码</a>
        </el-form-item>
      </el-form>

      <!-- <a href="#">忘记密码</a> -->
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      loginForm: {
        username: '',
        password: ''
      },
      rules: {
        username: [
          { required: true, message: '请输入用户名', trigger: 'blur' }
        ],
        password: [{ required: true, message: '请输入用户名', trigger: 'blur' }]
      }
    }
  }
}
</script>

<style lang="less" scoped>
.container {
  background: #2b4b6b;
  // background: url('../assets/image/login-bg.jpg') no-repeat;
  height: 100%;
}
.login_box {
  width: 450px;
  height: 300px;
  border-radius: 3px;
  background: #fff;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  .avatar_box {
    width: 130px;
    height: 130px;
    border: 1px solid #eee;
    border-radius: 50%;
    padding: 10px;
    box-shadow: 0 0 10px #ddd;
    position: absolute;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #fff;

    img {
      width: 100%;
      height: 100%;
      border-radius: 50%;
    }
  }
}
.btns{
    display: flex;
    justify-content: center;
}
.login_form{
    position: absolute;
    bottom: 0;
    width: 100%;
    padding: 0 20px;
    box-sizing: border-box;
}
</style>
