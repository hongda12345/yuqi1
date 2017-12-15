<template>
    <div>
        <el-form ref="form" :model="form" label-width="80px" :rules="rules">
            <el-form-item label="ID">
                {{form.pid}}
            </el-form-item>
            <el-form-item label="所属类型">
                <el-select v-model="form.tid" placeholder="请选择">
                    <el-option
                            v-for="item in options"
                            :key="item.tid"
                            :label="item.tname"
                            :value="item.tid">
                    </el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="人群名称" prop="pname">
                <el-input  type="text" v-model="form.pname"></el-input>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="submitForm('form')">提交</el-button>
            </el-form-item>
        </el-form>
    </div>
</template>
<script>
    export default{
        name:'peopleUpdate',
        data:function () {
            return{
                pid:'',
                value:'',
                form:{
                    pid:'',
                    value:'',
                },
                options: [
                    {

                    }
                ],
                rules: {

                }
            }
        },
        methods: {
            submitForm(formName) {
                this.$refs[formName].validate((valid) => {
                    if (valid) {
                        this.$http.post('/home/peopleUpdate.php',this.form).then(res=>{
                            if(res.body=='ok'){
                                this.$message({
                                    showClose: true,
                                    message:'恭喜你，修改成功',
                                    type:"success"
                                })
                                this.$router.push('managePeople');
                            }else if(res.body=='error'){
                                this.$message({
                                    showClose: true,
                                    message:'对不起，修改失败',
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
            this.pid=this.$route.query.pid;
            this.$http.get('/home/peopleQuery.php?pid='+this.pid).then(res=>{
                this.form=res.body;
            })
            this.$http.get('/home/manageType.php').then(res=>{
                this.options=res.body;
            })
        }
    }
</script>
<style>

</style>