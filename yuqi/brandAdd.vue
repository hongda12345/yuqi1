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
            <el-form-item label="品牌名称" prop="bname">
                <el-input  type="text" v-model="form.bname"></el-input>
            </el-form-item>
            <el-form-item label="品牌英文" prop="bename">
                <el-input  type="text" v-model="form.bename"></el-input>
            </el-form-item>
            <el-form-item label="品牌介绍" prop="bproduce">
                <el-input  type="text" v-model="form.bproduce"></el-input>
            </el-form-item>
            <el-form-item label="品牌标题" prop="btitle">
                <el-input  type="text" v-model="form.btitle"></el-input>
            </el-form-item>
            <el-form-item label="品牌图片" prop="bimage">
                <el-upload
                        class="upload-demo"
                        ref="upload"
                        multiple="false"
                        action="/home/uploadFile"
                        :on-preview="handlePreview"
                        :on-remove="handleRemove"
                        :on-change="handleChange"
                        :before-upload="beforeUpload"
                        :file-list="fileList"
                        :auto-upload="false"
                        :multiple="false"
                        list-type="picture">
                    <el-button slot="trigger" size="small" type="primary">选取文件</el-button>
                    <el-button style="margin-left: 10px;" size="small" type="success" @click="submitUpload">导入</el-button>
                    <div slot="tip" class="el-upload__tip">只能上传jpg/png文件，且不超过500kb</div>
                </el-upload>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="submitForm('form')">提交</el-button>
            </el-form-item>
        </el-form>
    </div>
</template>
<script>
    export default{
        name:'brandAdd',
        data:function () {
            return{
                form:{
                    bname:'',
                    bename:'',
                    bproduce:'',
                    btitle:'',
                    bimage:'',
                },
                fileList: [],
                options: [

                ],
                rules: {
                    bname: [
                        { required: true, message: '请输入方向名称', trigger: 'blur' },
                        { min: 1, max: 10, message: '长度在 1 到 10 个字符', trigger: 'blur' }
                    ],
                    bename: [
                        { required: true, message: '请输入方向名称', trigger: 'blur' },
                        { min: 1, max: 10, message: '长度在 1 到 10 个字符', trigger: 'blur' }
                    ],
                    bproduce: [
                        { required: true, message: '请输入方向名称', trigger: 'blur' },
                        { min: 1, max: 10, message: '长度在 1 到 10 个字符', trigger: 'blur' }
                    ],
                    btitle: [
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
                        this.$http.post('/home/brandAdd.php',this.form).then(res=>{
                            if(res.body=='ok'){
                                this.$message({
                                    showClose: true,
                                    message:'恭喜你，添加成功',
                                    type:"success"
                                })
                                this.$router.push('manageBrand');
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
            },
            submitUpload(){
                this.$refs.upload.submit();
            },
            handleRemove(file, fileList) {
                console.log(file, fileList);
            },
            handlePreview(file) {
                console.log(file);
            },
            handleChange(file,fileList){
                console.log(file);
                console.log(fileList);
            },
            beforeUpload:function(file){
                console.log(file);
                let fd=new FormData();
                fd.append('file',file);
                this.$http.post('/home/uploadFile',fd).then(res=>{
                    console.log(res);
                },res=>{
                    console.log(res);
                });
                return false;
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