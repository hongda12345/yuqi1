<template>
    <div>
        <div class="panel admin-panel">
            <div class="panel-head"><strong class="icon-reorder"> 内容列表</strong></div>
            <div class="padding border-bottom">
                <a class="button border-yellow" href=""><span class="icon-plus-square-o"></span><router-link :to="{name:'priceAdd'}"> 添加内容</router-link></a>
            </div>
            <el-table
                    :data="tableData"
                    stripe
                    style="width: 100%">
                <el-table-column
                        prop="rid"
                        label="ID"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="rname"
                        label="价格区间"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="tname"
                        label="所属类型"
                        width="180">
                </el-table-column>
                <el-table-column label="操作">
                    <template slot-scope="scope">
                        <el-button size="mini">
                            <router-link :to="{name:'priceUpdate',query:{rid:scope.row.rid}}">修改</router-link>
                        </el-button>
                        <el-button
                                size="mini"
                                type="danger"
                                @click="del(scope.row.rid)">删除
                        </el-button>
                    </template>
                </el-table-column>
            </el-table>
        </div>
    </div>
</template>
<script>
    export default {
        name:'managePrice',
        data() {
            return {
                tableData: [

                ]
            }
        },
        methods:{
            del(rid){
                this.$http.post('/home/priceDelete.php',{rid}).then(res=>{
                    if(res.body =='ok'){
                        this.tableData =  this.tableData.filter(ele=>ele.rid != rid);
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
            this.$http.post('/home/managePrice.php').then(res=>{
                this.tableData=res.body;
            });
        }
    }
</script>
<style>

</style>