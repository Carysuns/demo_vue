<template>
    <div>
        <h1>用户注册</h1>
        用户名:<el-input v-model="input" maxlength="11" placeholder="请输入用户名" style="width:300px"></el-input><br>
        密码:<el-input v-model="input" maxlength="11" style="width:300px" placeholder="请输入密码"></el-input><br>
        
        <el-button type="warning" @click="regist">注册</el-button>
    </div>
</template>
<script>
export default {

    data() {
        return {
            user: {}
        }
    },

    methods: {

        regist() {

            alert("good");
        }
    }
}
</script>
<style>

</style>