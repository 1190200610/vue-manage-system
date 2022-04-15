<template>
    <div class="">
        <div class="crumbs">
            <el-breadcrumb separator="/">
                <el-breadcrumb-item><i class="el-icon-lx-copy"></i>热榜话题</el-breadcrumb-item>
            </el-breadcrumb>
        </div>

        <el-table :data="tableData" stripe style="width: 100%">
          <el-table-column prop="topic_id" label="ID" width="180" />
          <el-table-column prop="topic_name" label="话题" width="180" />
          <el-table-column prop="link" label="链接" />

        </el-table>

    </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
    name: "tabs",
    setup() {

      const tableData = [
        {
          topic_id: '1',
          topic_name: '咸粽子销量是甜粽子4倍',
          link: 'https://s.weibo.com//weibo?q=%23%E5%92%B8%E7%B2%BD%E5%AD%90%E9%94%80%E9%87%8F%E6%98%AF%E7%94%9C%E7%B2%BD%E5%AD%904%E5%80%8D%23&Refer=top',
        },
        {
          topic_id: '2',
          topic_name: '齐司礼',
          link: 'https://s.weibo.com//weibo?q=%E9%BD%90%E5%8F%B8%E7%A4%BC&Refer=top',
        },
        {
          topic_id: '3',
          topic_name: '属于毕业的BGM',
          link: 'https://m.weibo.cn/search?containerid=100103type%3D1%26q%3D%23%E5%AE%89%E6%85%95%E5%B8%8C%E7%8E%AF%E4%BF%9D%E4%B8%8D%E5%A2%A8%E8%BF%B9%23',
        },
        {
          topic_id: '4',
          topic_name: '德普胜诉',
          link: 'https://s.weibo.com//weibo?q=%23%E5%BE%B7%E6%99%AE%E8%83%9C%E8%AF%89%23&Refer=top',
        },
      ]


        return {
            tableData,
        };
    },
};
</script>

<style>
.message-title {
    cursor: pointer;
}
.handle-row {
    margin-top: 30px;
}
</style>

