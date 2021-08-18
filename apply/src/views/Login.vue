<template>
  <div id="maindiv">
    <el-input class="inputtext" v-model="input" maxlength="11" placeholder="请输入用户名"></el-input><br>
    <el-input class="inputtext" placeholder="请输入密码" maxlength="11" v-model="password" show-password></el-input>
    <el-row id="button1">
      <el-button type="warning" @click="login">登录</el-button>
      <el-button type="danger" @click="cancel">取消</el-button>
    </el-row><br>
    <img id ="loginimg" src="../assets/IMG_20210613_141339 .jpg">
  </div>
</template>
<script>
export default {
  data() {
    return {
      input: '',
      password: '',
      user: {}
    }
  },

  methods: {

    login() {

      // 用户名为空的检查
      if (this.input === '') {

        alert('用户名不能为空');
        return;
      }

      // 密码为空的检查
      if (this.password === '') {
        
        alert('密码不能为空');
        return;
      }

      // 密码长度的检查
      if (this.password.length < 8 || this.password.length > 16) {

        alert('密码需要在8~16位');
        return;
      }

      const username = this.input;
      const psd = this.password;
      const url = 'http://localhost:8080/user/username?user_name=' + username + '&password=' + psd;
      
      this.$axios.get(url)
        .then(function (response) {
          console.log(response);
          this.user = response.data.users;
        })

      window.location.href="http://localhost:8090/#/user";
    },

    cancel() {

      this.input='';
      this.password='';
    }
  }
}
</script>

<style>
#button1 {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}

.inputtext {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 5px;
  margin-bottom: 5px;
  width: 500px;
}

#loginimg {

  width: 400px;
}
</style>