<template>
  <div>
    <el-radio v-model="radio"
              label="1">备选项</el-radio>
    <el-radio v-model="radio"
              label="2">备选项</el-radio>
    <el-row>
      <el-radio v-model="radio1"
                label="禁用"
                disabled>备选项</el-radio>
      <el-radio v-model="radio1"
                label="选中且禁用"
                disabled>备选项</el-radio>
    </el-row>
    <el-row>
      <el-radio-group v-model="radio2">
        <el-radio :label="3">备选项</el-radio>
        <el-radio :label="6">备选项</el-radio>
        <el-radio :label="9">备选项</el-radio>
      </el-radio-group>
    </el-row>
    <el-row>
      <el-radio-group v-model="radio3">
        <el-radio-button label="上海"></el-radio-button>
        <el-radio-button label="北京"></el-radio-button>
        <el-radio-button label="广州"></el-radio-button>
        <el-radio-button label="深圳"></el-radio-button>
      </el-radio-group>
    </el-row>
    <el-row>
      <el-radio v-model="radio7"
                label="1"
                border="true"></el-radio>
      <el-radio v-model="radio7"
                label="2"
                border="true"></el-radio>

    </el-row>
  </div>

</template>

<script>
export default {
  name: 'ELRadioDemo',
  data () {
    return {
      radio: '1',
      radio1: '禁用',
      radio2: 3,
      radio3: '上海',
      radio7: '1'
    };
  }
}
</script>

<style scoped>
</style>

