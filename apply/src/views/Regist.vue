<template>
    <div>
        <h1>用户注册</h1>
        <form>
            <label>昵称:</label><el-input v-model="username" maxlength="11" placeholder="请输入用户名" style="width:300px"></el-input><br>
            <label>密码:</label><el-input v-model="password" maxlength="11" style="width:300px" placeholder="请输入密码"></el-input><br>
            <label>邮箱:</label><el-input v-model="email" maxlength="20" style="width:300px" placeholder="请输入邮箱"></el-input><br>
            <label>年龄:</label><el-input type="number" v-model="age" maxlength="20" style="width:300px" placeholder="请输入年龄"></el-input><br>
            <label>生日:</label><el-input type="date" v-model="birthday" maxlength="20" style="width:300px"></el-input><br>
            <label>国籍:</label><el-input v-model="country" maxlength="20" style="width:300px" placeholder="请输入国籍"></el-input><br>
            <label>省份:</label><el-input v-model="province" maxlength="20" style="width:300px" placeholder="请输入省份"></el-input><br>
            <label>城市:</label><el-input v-model="city" maxlength="20" style="width:300px" placeholder="请输入城市"></el-input><br>
            <label>性别: </label>男<input type="radio" v-model="sex" name="sex" value="male">女<input type="radio" v-model="sex" name="sex" value="female"><br>
            <label>身高:</label><el-input v-model="height" maxlength="20" style="width:300px" placeholder="请输入身高"></el-input><br>
            <label>院校:</label><el-input v-model="collage" maxlength="30" style="width:300px" placeholder="请输入毕业院校"></el-input><br>
            <label>职业:</label><el-input v-model="
            occupation" maxlength="20" style="width:300px" placeholder="请输入职业"></el-input><br>
            <label>爱好: </label>唱歌<input type="checkbox" v-model="hobby" value="music">
                                喝酒<input type="checkbox" v-model="hobby" value="peer">
                                交友<input type="checkbox" v-model="hobby" value="friends">
                                学习<input type="checkbox" v-model="hobby" value="study"><br>
            <label>个人简介:</label><textarea></textarea><br>
            <el-button type="warning" @click="regist">注册</el-button>
            <el-button type="danger" @click="goLogin">返回登录</el-button>
        </form>
        
    </div>
</template>
<script>
export default {

    data() {
        return {
            username: '',
            password: '',
            email: '',
            age: '',
            birthday: '',
            country: '',
            province: '',
            city: '',
            sex: '',
            height: '',
            collage: '',
            occupation: '',
            hobby: [],
            user: {}
        }
    },

    methods: {

        regist() {
            
            alert("good");
        },

        goLogin() {

            window.location.href="http://localhost:8090/#/login";
        }
    }
}
</script>
<style>

</style>