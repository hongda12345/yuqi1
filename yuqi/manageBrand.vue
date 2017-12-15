<template>
    <div>
        <div class="panel admin-panel">
            <div class="panel-head"><strong class="icon-reorder"> 内容列表</strong></div>
            <div class="padding border-bottom">
                <a class="button border-yellow" href=""><span class="icon-plus-square-o"></span><router-link :to="{name:'brandAdd'}"> 添加内容</router-link></a>
            </div>
            <el-table
                    :data="tableData"
                    stripe
                    style="width: 100%">
                <el-table-column
                        prop="bid"
                        label="ID"
                        width="60">
                </el-table-column>
                <el-table-column
                        prop="bname"
                        label="品牌名称"
                        width="100">
                </el-table-column>
                <el-table-column
                        prop="bename"
                        label="品牌英文"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="bproduce"
                        label="品牌介绍"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="btitle"
                        label="品牌标题"
                        width="100">
                </el-table-column>
                <el-table-column
                        prop="bimage"
                        label="品牌图片"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="tname"
                        label="所属类型"
                        width="100">
                </el-table-column>
                <el-table-column label="操作">
                    <template slot-scope="scope">
                        <el-button size="mini">
                            <router-link :to="{name:'brandUpdate',query:{bid:scope.row.bid}}">修改</router-link>
                        </el-button>
                        <el-button
                                size="mini"
                                type="danger"
                                @click="del(scope.row.bid)">删除
                        </el-button>
                    </template>
                </el-table-column>
            </el-table>
        </div>
    </div>
</template>
<script>
    export default {
        name:'manageBrand',
        data() {
            return {
                tableData: [

                ]
            }
        },
        methods:{
            del(bid){
                this.$http.post('/home/brandDelete.php',{bid}).then(res=>{
                    if(res.body =='ok'){
                        this.tableData =  this.tableData.filter(ele=>ele.bid != bid);
                    }else if(res.body =='error'){
                        this.$message({
                            showClose: true,
                            message: '删除失败',
                            type: 'error'
                        });
                    }
                })
            }
        },
        mounted(){
            this.$http.post('/home/manageBrand.php').then(res=>{
                this.tableData=res.body;
            });
        }
    }
</script>
<style>

</style>