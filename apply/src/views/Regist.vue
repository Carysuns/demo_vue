<template>
    <div class="regist">
        <el-row>
            <el-col :span="24">
                <h1>用户注册</h1>
                <el-form 
                    :model="loginForm"
                    ref="loginForm">
                        <el-row class="row">
                            <el-col :span="9" class="title">用户名:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.username" class="input">
                                    <el-input v-model="username" maxlength="11" placeholder="请输入用户名"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">昵称:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.nickname" class="input">
                                    <el-input v-model="nickname" maxlength="11" placeholder="请输入昵称"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">密码:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.password" class="input">
                                    <el-input v-model="password" maxlength="16" placeholder="请输入密码"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">邮箱:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.email" class="input">
                                    <el-input v-model="email" maxlength="20" placeholder="请输入邮箱"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">年龄:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.age" class="input">
                                    <el-input v-model="age" type="number" maxlength="3" placeholder="请输入年龄"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">生日:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.birthday" class="input">
                                    <el-input v-model="birthday" type="date" maxlength="20" placeholder="请输入生日"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">国籍:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.country" class="input">
                                    <el-input v-model="country" maxlength="20" placeholder="请输入国籍"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">省份:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.province" class="input">
                                    <el-input v-model="province" maxlength="20" placeholder="请输入省份"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">城市:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.city" class="input">
                                    <el-input v-model="city" maxlength="20" placeholder="请输入城市"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">性别:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.city" class="input">
                                    男<input type="radio" v-model="sex" name="sex" value="male">
                                    女<input type="radio" v-model="sex" name="sex" value="female">
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">身高:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.height" class="input">
                                    <el-input v-model="height" maxlength="11" placeholder="请输入身高"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">院校:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.collage" class="input">
                                    <el-input v-model="collage" maxlength="30" placeholder="请输入院校"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">职业:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.occupation" class="input">
                                    <el-input v-model="occupation" maxlength="20" placeholder="请输入职业"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">爱好:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.hobby" class="input">
                                    <el-input v-model="hobby" type="textarea" :rows="3" placeholder="请输入爱好"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                        <el-row>
                            <el-col :span="9" class="title">个人简介:</el-col>
                            <el-col :span="15">
                                <el-form-item prop="loginForm.note" class="input">
                                    <el-input v-model="note" type="textarea" :rows="3" placeholder="请输入个人简介"></el-input>
                                </el-form-item>
                            </el-col>
                        </el-row>
                    <el-button type="warning" @click="regist">注册</el-button>
                    <el-button type="danger" @click="goLogin">返回登录</el-button>
                </el-form>
            </el-col>
        </el-row>
    </div>
</template>
<script>
export default {

    data() {
        return {
            username: '',
            nickname: '',
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
            hobby: '',
            user: {}
        }
    },

    methods: {

        regist() {
            
            alert("请填写信息");
        },

        goLogin() {

            window.location.href="http://localhost:8090/#/login";
        }
    }
}
</script>
<style>
.title {
    text-align: right;
    vertical-align: center;
}
.input {
    text-align: left;
    width: 500px;
    margin-left: 50px;
}
</style>