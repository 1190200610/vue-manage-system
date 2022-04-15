<template>
    <div>
        <div class="crumbs">
            <el-breadcrumb separator="/">
                <el-breadcrumb-item>
                    <i class="el-icon-pie-chart"></i>舆论领袖查询
                </el-breadcrumb-item>
            </el-breadcrumb>
        </div>
        <div class="container">






        </div>
    </div>
</template>

<script>
import Schart from "vue-schart";
export default {
    name: "basecharts",
    components: {
        Schart,
    },
    setup() {
        const options1 = {};
        const options2 = {};
        const options3 = {};
        const options4 = {};
        return {
            options1,
            options2,
            options3,
            options4,
        };
    },
};
</script>

<style scoped>
.schart-box {
    display: inline-block;
    margin: 20px;
}
.schart {
    width: 600px;
    height: 400px;
}
.content-title {
    clear: both;
    font-weight: 400;
    line-height: 50px;
    margin: 10px 0;
    font-size: 22px;
    color: #1f2f3d;
}
</style>