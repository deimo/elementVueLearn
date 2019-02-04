<template>
  <div>
    <el-row>
      <el-select v-model="value"
                 placeholder="请选择">
        <el-option v-for="item in options"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value"
                   :disabled="item.disabled">
        </el-option>
      </el-select>
    </el-row>
    <el-row>
      <el-select v-model="value"
                 placeholder="请选择"
                 disabled>
        <el-option v-for="item in options"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value"
                   :disabled="item.disabled">
        </el-option>
      </el-select>
    </el-row>
    <el-row>
      <el-select v-model="value4"
                 clearable
                 placeholder="请选择">
        <el-option v-for="item in options"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value">
        </el-option>
      </el-select>
    </el-row>
    <el-row>
      <el-select v-model="value5"
                 multiple
                 placeholder="请选择">
        <el-option v-for="item in options"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value">
        </el-option>
      </el-select>
      <el-select v-model="value11"
                 multiple
                 collapse-tags
                 style="margin-left: 20px;"
                 placeholder="请选择">
        <el-option v-for="item in options"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value">
        </el-option>

      </el-select>
    </el-row>
    <el-row>
      <el-select v-model="value6"
                 placeholder="请选择">
        <el-option v-for="item in cities"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value">
          <span style="float: left;">{{ item.label }}</span>
          <span style="float: right; color:#8492a6; font-size: 13px">{{ item.value }}</span>
        </el-option>
      </el-select>
    </el-row>
    <el-row>
      <el-select v-model="value7"
                 placeholder="请选择">
        <el-option-group v-for="group in options3"
                         :key="group.label"
                         :label="group.label">
          <el-option v-for="item in group.options"
                     :key="item.value"
                     :label="item.label"
                     :value="item.value">
          </el-option>

        </el-option-group>
      </el-select>
    </el-row>
    <el-row>
      <el-select v-model="value8"
                 filterable
                 placeholder="请选择">
        <el-option v-for="item in options"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value">
        </el-option>
      </el-select>
    </el-row>
    <el-row>
      <el-select v-model="value10"
                 multiple
                 filterable
                 allow-create
                 default-first-option
                 placeholder="请选择文章标签">
        <el-option v-for="item in options5"
                   :key="item.value"
                   :label="item.label"
                   :value="item.value">
        </el-option>
      </el-select>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'ElSelectDemo',
  data () {
    return {
      options: [
        {
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶',
          disabled: true,
        }, {
          value: '选项3',
          label: '蚵仔煎',
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }
      ],
      cities: [{
        value: 'Beijing',
        label: '北京'
      }, {
        value: 'Shanghai',
        label: '上海'
      }, {
        value: 'Nanjing',
        label: '南京'
      }, {
        value: 'Chengdu',
        label: '成都'
      }, {
        value: 'Shenzhen',
        label: '深圳'
      }, {
        value: 'Guangzhou',
        label: '广州'
      }],
      options3: [{
        label: '热门城市',
        options: [{
          value: 'Shanghai',
          label: '上海'
        }, {
          value: 'Beijing',
          label: '北京'
        }]
      }, {
        label: '城市名',
        options: [{
          value: 'Chengdu',
          label: '成都'
        }, {
          value: 'Shenzhen',
          label: '深圳'
        }, {
          value: 'Guangzhou',
          label: '广州'
        }, {
          value: 'Dalian',
          label: '大连'
        }]
      }],
      options5: [{
        value: 'HTML',
        label: 'HTML'
      }, {
        value: 'CSS',
        label: 'CSS'
      }, {
        value: 'JavaScript',
        label: 'JavaScript'
      }],
      value: '',
      value4: '',
      value5: [],
      value6: '',
      value7: '',
      value8: '',
      value10: [],
      value11: [],
    }
  }
}
</script>


<style>
</style>