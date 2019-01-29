<template>
  <div>
    <el-row>
      <el-button>默认按钮</el-button>
      <el-button type="primary"
                 size="medium">主要按钮 中</el-button>
      <el-button type="success"
                 size="small">成功按钮 小</el-button>
      <el-button type="info"
                 size="mini">信息按钮 超小</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>
    </el-row>
    <el-row>
      <el-button plain>朴素按钮</el-button>
      <el-button type="primary"
                 plain>主要按钮</el-button>
      <el-button type="success"
                 plain>成功按钮</el-button>
      <el-button type="info"
                 plain>信息按钮</el-button>
      <el-button type="warning"
                 plain>警告按钮</el-button>
      <el-button type="danger"
                 plain
                 disabled>危险按钮</el-button>
    </el-row>
    <el-row>
      <el-button round>圆角按钮</el-button>
      <el-button type="primary"
                 round>主要按钮</el-button>
      <el-button type="success"
                 round>成功按钮</el-button>
      <el-button type="info"
                 round>信息按钮</el-button>
      <el-button type="warning"
                 round>警告按钮</el-button>
      <el-button type="danger"
                 round
                 disabled>危险按钮</el-button>
    </el-row>
    <el-row>
      <el-button icon="el-icon-search"
                 circle></el-button>
      <el-button icon="el-icon-edit"
                 type="primary"
                 circle></el-button>
      <el-button type="success"
                 icon="el-icon-check"
                 circle></el-button>
      <el-button type="info"
                 icon="el-icon-message"
                 circle></el-button>
      <el-button type="warning"
                 icon="el-icon-star-off"
                 circle></el-button>
      <el-button type="danger"
                 icon="el-icon-delete"
                 circle
                 disabled></el-button>
    </el-row>
    <el-row>
      <el-button type="text">文字按钮</el-button>
      <el-button type="text"
                 disabled>文字按钮</el-button>
    </el-row>
    <el-row>
      <el-button type="primary"
                 icon="el-icon-edit"></el-button>
      <el-button type="primary"
                 icon="el-icon-share"></el-button>
      <el-button type="primary"
                 icon="el-icon-delete"></el-button>
      <el-button type="primary"
                 icon="el-icon-search">搜索</el-button>
      <el-button type="primary">
        上传
        <i class="el-icon-upload"></i>
      </el-button>
    </el-row>
    <el-row :gutter="20">
      <el-col :span="12">
        <el-button-group>
          <el-button type="primary"
                     icon="el-icon-arrow-left">上一页</el-button>
          <el-button type="primary">下一页
            <i class="el-icon--right el-icon-arrow-right"></i>
          </el-button>
        </el-button-group>
      </el-col>
      <el-col :span="12">
        <el-button-group>
          <el-button type="primary"
                     icon="el-icon-edit"></el-button>
          <el-button type="primary"
                     icon="el-icon-share"></el-button>
          <el-button type="primary"
                     icon="el-icon-delete"></el-button>
        </el-button-group>
      </el-col>
    </el-row>
    <el-button type="primary"
               :loading="true">加载中</el-button>
  </div>

</template>

<script>
export default {
  name: 'ElMyButton'
}
</script>

<style>
</style>