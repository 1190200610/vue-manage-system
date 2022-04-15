<template>
    <div>
        <div class="crumbs">
            <el-breadcrumb separator="/">
                <el-breadcrumb-item>
                    <i class="el-icon-lx-emoji"></i>话题评论
                </el-breadcrumb-item>
            </el-breadcrumb>
        </div>
        <div class="container">
<!--          Panel-->
            <div class="demo-collapse">
              <el-collapse v-model="activeName" accordion>
                <el-collapse-item title="Consistency" name="1">

                  <div>
                      <el-descriptions title="User Info">
                        <el-descriptions-item label="Username">kooriookami</el-descriptions-item>
                        <el-descriptions-item label="Telephone">18100000000</el-descriptions-item>
                        <el-descriptions-item label="Place">Suzhou</el-descriptions-item>
                        <el-descriptions-item label="Remarks">
                          <el-tag size="small">School</el-tag>
                        </el-descriptions-item>
                        <el-descriptions-item label="Address"
                        >No.1188, Wuzhong Avenue, Wuzhong District, Suzhou, Jiangsu
                          Province</el-descriptions-item
                        >
                      </el-descriptions>
                  </div>

                </el-collapse-item>
                <el-collapse-item title="Feedback" name="2">
                  <div>
                    Operation feedback: enable the users to clearly perceive their
                    operations by style updates and interactive effects;
                  </div>
                  <div>
                    Visual feedback: reflect current state by updating or rearranging
                    elements of the page.
                  </div>
                </el-collapse-item>
                <el-collapse-item title="Efficiency" name="3">
                  <div>
                    Simplify the process: keep operating process simple and intuitive;
                  </div>
                  <div>
                    Definite and clear: enunciate your intentions clearly so that the
                    users can quickly understand and make decisions;
                  </div>
                  <div>
                    Easy to identify: the interface should be straightforward, which helps
                    the users to identify and frees them from memorizing and recalling.
                  </div>
                </el-collapse-item>
                <el-collapse-item title="Controllability" name="4">
                  <div>
                    Decision making: giving advices about operations is acceptable, but do
                    not make decisions for the users;
                  </div>
                  <div>
                    Controlled consequences: users should be granted the freedom to
                    operate, including canceling, aborting or terminating current
                    operation.
                  </div>
                </el-collapse-item>
              </el-collapse>
            </div>



        </div>
    </div>
</template>

<script>
import { computed, ref } from "vue";
export default {
    name: "icon",
    setup() {
        const iconList = [];
        const keyword = ref("");
        const list = computed(() => {
            return iconList.filter((item) => {
                return item.indexOf(keyword.value) !== -1;
            });
        });

        return {
            iconList,
            keyword,
            list,
        };
    },
};
</script>

<style scoped>
.example-p {
    height: 45px;
    display: flex;
    align-items: center;
}
.search-box {
    text-align: center;
    margin-top: 10px;
}
.search {
    width: 300px;
}
ul,
li {
    list-style: none;
}
.icon-li {
    display: inline-block;
    padding: 10px;
    width: 120px;
    height: 120px;
}
.icon-li-content {
    display: flex;
    height: 100%;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}
.icon-li-content i {
    font-size: 36px;
    color: #606266;
}
.icon-li-content span {
    margin-top: 10px;
    color: #787878;
}
</style>