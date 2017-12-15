<template>
    <div>
        <el-form ref="form" :model="form" label-width="80px" :rules="rules">
            <el-form-item label="所属类型">
                <el-select v-model="form.value" placeholder="请选择">
                    <el-option
                            v-for="item in options"
                            :key="item.tid"
                            :label="item.tname"
                            :value="item.tid">
                    </el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="类型名称" prop="mename">
                <el-input  type="text" v-model="form.mename"></el-input>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="submitForm('form')">提交</el-button>
            </el-form-item>
        </el-form>
    </div>
</template>
<script>
    export default{
        name:'materAdd',
        data:function () {
            return{
                form:{
                    mename:'',
                },
                options: [

                ],
                rules: {
                    mename: [
                        { required: true, message: '请输入方向名称', trigger: 'blur' },
                        { min: 1, max: 10, message: '长度在 1 到 10 个字符', trigger: 'blur' }
                    ],
                }
            }
        },
        methods: {
            submitForm(formName) {
                this.$refs[formName].validate((valid) => {
                    if (valid) {
                        this.$http.post('/home/materAdd.php',this.form).then(res=>{
                            if(res.body=='ok'){
                                this.$message({
                                    showClose: true,
                                    message:'恭喜你，添加成功',
                                    type:"success"
                                })
                                this.$router.push('manageMater');
                            }else if(res.body=='error'){
                                this.$message({
                                    showClose: true,
                                    message:'对不起，添加失败',
                                    type:"error"
                                })
                            }
                        })
                    } else {
                        console.log('error submit!!');
                        return false;
                    }
                });
            }
        },
        mounted(){
            this.$http.get('/home/manageType.php').then(res=>{
                this.options=res.body;
            })
        }
    }
</script>
<style>

</style>