<template>
  <div>
    <el-input v-model="input" placeholder="请输入用户名"></el-input>
    <el-input placeholder="请输入密码" v-model="password" show-password></el-input>
    <el-row id="button1">
      <el-button type="warning" @click="login">登录</el-button>
      <el-button type="danger" @click="cancel">注销</el-button>
    </el-row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      input: '',
      password: ''
    }
  },

  methods: {

    login() {
      window.location.href="http://localhost:8090/#/user";
    },

    cancel() {
      this.input='';
      this.password='';
    }
  }
}
</script>