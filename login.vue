<template>
    <div class="login_container">
        <div class="login_box">
        <!--  登录表单  -->
            <el-form :model="loginForm" class="login_form">
                <!--  账号  -->
                <el-form-item>
                    <el-input v-model="loginForm.account" prefix-icon="el-icon-user"></el-input>
                </el-form-item>
                <!--  密码  -->
                <el-form-item>
                    <el-input show-password v-model="loginForm.password" prefix-icon="el-icon-lock"></el-input>
                </el-form-item>
                <!--  按钮  -->
                <el-form-item class="login_btn">
                    <el-button type="primary">登录</el-button>
                    <el-button type="info">重置</el-button>
                </el-form-item>
             </el-form>
        </div>
    </div>

</template>
<script>
    export default {
        name: "login",
        data(){
            return{
                loginForm:{
                    account:'',
                    password:'',
                }
            }

        }
    }
</script>

<style lang="less" scoped>
    .login_container{
        background-color: cadetblue;
        height: 100%;
    }

    .login_title {
        font-size: 38px;
        font-family: 华文中宋;
        color: rgba(248, 247, 247, 0.98);
        text-align: center;
        /*margin-top: 10px;*/
    }
    .login_form{
        position: absolute;
        bottom: 30px;
        width: 100%;
        padding: 0 20px;
        box-sizing: border-box;
    }
    .login_box {
        width: 450px;
        height: 300px;
        background-color: #f9fdff;
        border-radius: 18px;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
    }
    .login_btn {
        display: flex;
        justify-content: flex-end;
        /*align-content: center;*/
    }
</style>