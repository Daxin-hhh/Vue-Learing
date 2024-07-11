<template>
  <div>
    <my-date-picker
      v-model="date"
      type="dates"
      placeholder="Pick one or more dates"
      @change="deteChange"
    >
    </my-date-picker>
    <el-divider />
    <div class="login">
      <el-form :model="formData" >
        <el-form-item label="账号">
          <my-input v-model="formData.account" clearable></my-input>
        </el-form-item>
        <el-form-item label="密码">
          <my-input v-model="formData.password" type="password" clearable></my-input>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="onSubmit">登录</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import MyDatePicker from "./MyDatePicker.vue";
import MyInput from "./MyInput.vue";
export default {
  components: { MyDatePicker, MyInput },
  data() {
    return {
      date: "",
      formData: {
        account: "",
        password: "",
      },
    };
  },
  methods: {
    deteChange() {
      console.log("日期数据修改了");
    },
	onSubmit(){}
  },
};
</script>
<style scoped>
.login {
  width: 500px;
  height: 400px;
  border: 1px solid pink;
  display: flex;
  justify-content: center;
  padding-top: 50px;
}
</style>
