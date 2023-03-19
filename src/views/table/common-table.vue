<template>
    <div class="table_container">
        <el-table 
            :data="tableData" 
            v-loading="loading"
            border
        >
            <el-table-column 
                v-for="item,index in columns" 
                :key="index" 
                :label="item.label" 
                align="center"
                :prop="item.prop" 
                :fixed="item.fixed"
                :width="item.width?item.width:''"
                :show-overflow-tooltip="!!item.width"
            ></el-table-column>
            <el-table-column align="center" label="操作" fixed="right" width="180">
                <template slot-scope="scope">
                    <el-button type="text" @click="hanleEdit(scope.row)">编辑</el-button>
                    <el-button type="text" @click="hanleDelete(scope.row)">删除</el-button>
                </template>
            </el-table-column>
        </el-table>
    </div>
</template>

<script>
export default {
    data(){
        return {
            loading: false,
            tableData: [
                { emplId: '111', name: '222' }
            ],
            columns: [
                { label:'员工ID', prop:'emplId', fixed:'left', width: '100' },
                { label:'姓名', prop:'name', fixed:'left', width: '100' },
                { label:'在职状态', prop:'hrStatus' },
                { label:'体系', prop:'hpsDeptType1' },
                { label:'板块', prop:'hpsDeptType2' },
                { label:'中心/区域', prop:'hpsDeptType4', width:'100' },
                {label:'片区', prop:'hpsDeptType5' },
                { label:'部门/分公司', prop:'hpsDeptType6', width:'120' },
                { label:'团队/财富管理中心', prop:'hpsDeptType7', width:'180'  },
                { label:'团队/财富管理中心', prop:'hpsDeptType7', width:'180'  },
                { label:'团队/财富管理中心', prop:'hpsDeptType7', width:'180'  },
                { label:'团队/财富管理中心', prop:'hpsDeptType7', width:'180'  },
                { label:'团队/财富管理中心', prop:'hpsDeptType7', width:'180'  },
                { label:'团队/财富管理中心', prop:'hpsDeptType7', width:'180' },
            ],
        }
    },
    methods: {
        hanleEdit(){

        },
        hanleDelete(){

        },
    }
}
</script>

<style lang="scss" scoped>
.table_container {
    padding: 20px;
}
</style>