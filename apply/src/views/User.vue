<template>
  <div>
    <table>
      <tr>
        <th>编号</th>
        <th>名字</th>
        <th>年龄</th>
        <th>性别</th>
        <th>国籍</th>
        <th>省份</th>
        <th>城市</th>
        <th>身高</th>
        <th>个人简介</th>
        <th>职业</th>
        <th>毕业院校</th>
        <th>出生日期</th>
        <th>爱好</th>
      </tr>
      <tr v-for = "item in users">
        <td>{{item.id}}</td>
        <td>{{item.user_name}}</td>
        <td>{{item.age}}</td>
        <td>{{item.sex == 0? '男' : '女'}}</td>
        <td>{{item.nation}}</td>
        <td>{{item.province}}</td>
        <td>{{item.city}}</td>
        <td>{{item.height}}</td>
        <td>{{item.note}}</td>
        <td>{{item.occupation}}</td>
        <td>{{item.collage}}</td>
        <td>{{item.birthday}}</td>
        <td>{{item.hobby}}</td>
      </tr>
    </table>
    <button v-on:click="show">点我</button>
  </div>
</template>

<script>
  export default {
    name: "user",
    data(){
      return {
        msg: "hello world",
        users: {},
      }
    },

    created () {
      const that = this;
      this.$axios.get('http://localhost:8080/user')
        .then(function (response) {
          console.log(response);
          that.users = response.data.users;
        })
    }
  }

  function show(){

    alert(1);
  }
    
</script>
<style scoped>
</style>