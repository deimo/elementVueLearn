<template>
  <div>
    <el-input v-model="input"
              placeholder="请输入内容">
    </el-input>
    <el-input v-model="input1"
              placeholder="请输入内容"
              :disabled="true">
    </el-input>
    <el-input placeholder="请输入内容"
              v-model="input10"
              clearable>
    </el-input>
    <el-row>
      <div class="demo-input-suffix">
        属性方式：
        <el-input placeholder="请选择日期"
                  suffix-icon="el-icon-date"
                  v-model="input2">
        </el-input>
        <el-input placeholder=请输入内容
                  prefix-icon="el-icon-search"
                  v-model="input21">
        </el-input>
      </div>
    </el-row>
    <el-row>
      <div class="demo-input-suffix">
        slot方式：
        <el-input placeholder="请选择日期"
                  v-model="input22">
          <i slot="suffix"
             class="el-input__icon el-icon-date"></i>
        </el-input>
        <el-input placeholder="请输入内容"
                  v-model="input23">
          <i slot="prefix"
             class="el-input__icon el-icon-search"></i>
        </el-input>
      </div>
    </el-row>
    <el-row>
      <el-input type="textarea"
                :rows="2"
                placeholder="请输入内容"
                v-model="textarea">

      </el-input>
      <el-input type="textarea"
                autosize
                placeholder="请输入内容"
                v-model="textarea2">
      </el-input>
      <div style="margin: 20px 0;"></div>
      <el-input type="textarea"
                :autosize="{minRows: 2, maxRows: 4}"
                placeholder="请输入内容"
                v-model="textarea3">
      </el-input>
    </el-row>
    <div>
      <el-input placeholder="请输入内容"
                v-model="input3">
        <template slot="prepend">Http://</template>
      </el-input>
    </div>
    <div style="margin-top: 15px;">
      <el-input placeholder="请输入内容"
                v-model="input4">

        <template slot="append">.com</template>
      </el-input>
    </div>
    <div style="margin-top: 15px;">
      <el-input placeholder="请输入内容"
                v-model="input5"
                class="input-with-select">
        <el-select v-model="select"
                   slot="prepend"
                   placeholder="请选择">
          <el-option label="餐厅名"
                     value="1"></el-option>
          <el-option label="订单号"
                     value="2"></el-option>
          <el-option label="用户电话"
                     value="3"></el-option>
        </el-select>
        <el-button slot="append"
                   icon="el-icon-search">
        </el-button>
      </el-input>
      <div class="demo-input-size">
        <el-input placeholder="请输入内容"
                  suffix-icon="el-icon-date"
                  v-model="input6">
        </el-input>
        <el-input size="medium"
                  placeholder="请输入内容"
                  suffix-icon="el-icon-date"
                  v-model="input7">
        </el-input>
        <el-input size="small"
                  placeholder="请输入内容"
                  suffix-icon="el-icon-date"
                  v-model="input8">
        </el-input>
        <el-input size="mini"
                  placeholder="请输入内容"
                  suffix-icon="el-icon-date"
                  v-model="input9">
        </el-input>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ElInputDemo',
  data () {
    return {
      input: '',
      input1: '',
      input10: '',
      input2: '',
      input21: '',
      input22: '',
      input23: '',
      input6: '',
      input7: '',
      input8: '',
      input9: '',
      textarea: '',
      textarea2: '',
      textarea3: '',
      select: '',
    }
  }
}
</script>

<style>
.el-select .el-input {
  width: 130px;
}
.input-with-select .el-input-group__prepend {
  background-color: #fff;
}
</style>
