<template>
  <div>
    <el-checkbox v-model="checked">备选项</el-checkbox>
    <el-row>
      <el-checkbox v-model="checked1">备选项</el-checkbox>
      <el-checkbox v-model="checked2"
                   disabled>备选项</el-checkbox>
    </el-row>
    <el-row>
      <el-chekbox-group v-model="checkList">
        <el-checkbox label="复选框 A"></el-checkbox>
        <el-checkbox label="复选框 B"></el-checkbox>
        <el-checkbox label="复选框 C"></el-checkbox>
        <el-checkbox label="禁用"
                     disabled></el-checkbox>
        <el-checkbox label="选中且禁用"
                     disabled></el-checkbox>
      </el-chekbox-group>
    </el-row>
    <el-row>
      <el-checkbox :indeterminate="isIndeterminate"
                   v-model="checkAll"
                   @change="handleCheckAllChange">全选</el-checkbox>
      <div style="margin: 15px 0;"></div>
      <el-checkbox-group v-model="checkedCities"
                         @change="handleCheckedCitiesChange">
        <el-checkbox v-for="city in cities"
                     :label="city"
                     :key="city">{{ city }}</el-checkbox>
      </el-checkbox-group>
    </el-row>
    <el-row>
      <el-checkbox-group v-model="checkedCities1"
                         :min="1"
                         :max="2">
        <el-checkbox v-for="city in cities"
                     :label="city"
                     :key="city">{{city}}</el-checkbox>
      </el-checkbox-group>
    </el-row>
    <el-row>
      <el-checkbox-group v-model="checkboxGroup1">
        <el-checkbox-button v-for="city in cities"
                            :key="city"
                            :label="city">{{ city }}</el-checkbox-button>
      </el-checkbox-group>
    </el-row>
    <div style="margin-top: 20px"></div>
    <el-row>
      <el-checkbox-group v-model="checkboxGroup2"
                         size="medium">
        <el-checkbox-button v-for="city in cities"
                            :key="city"
                            :label="city">{{ city }}</el-checkbox-button>
      </el-checkbox-group>
    </el-row>
    <div style="margin-top: 20px">
    </div>
    <el-row>
      <el-checkbox-group v-model="checkboxGroup3"
                         size="small">
        <el-checkbox-button v-for="city in cities"
                            :key="city"
                            :label="city">{{ city }}</el-checkbox-button>
      </el-checkbox-group>
    </el-row>
    <div style="margin-top: 20px;"></div>
    <el-row>
      <el-checkbox-group v-model="checkboxGroup4"
                         size="mini">
        <el-checkbox-button v-for="city in cities"
                            :key="city"
                            :label="city">{{ city }}</el-checkbox-button>
      </el-checkbox-group>
    </el-row>
    <el-row>
      <el-checkbox v-model="checked3"
                   label="备选项1"
                   border></el-checkbox>
      <el-checkbox v-model="checked4"
                   label="备选项2"
                   border></el-checkbox>
    </el-row>
    <div style="margin-top: 20px;"></div>
    <el-row>
      <el-checkbox v-model="checked5"
                   label="备选项1"></el-checkbox>
      <el-checkbox v-model="checked6"
                   label="备选项2"></el-checkbox>
    </el-row>
    <div style="margin-top: 20px;"></div>
    <el-row>
      <el-checkbox-group v-model="checkboxGroup5"
                         size="small">
        <el-checkbox label="备选项1"
                     border></el-checkbox>
        <el-checkbox label="备选项2"
                     border></el-checkbox>
      </el-checkbox-group>
    </el-row>
  </div>
</template>

<script>
const cityOptions = ['上海', '北京', '广州', '深圳'];
export default {
  name: 'ElCheckBoxDemo',
  data () {
    return {
      checkAll: false,
      checked: true,
      checked1: false,
      checked2: true,
      checked3: true,
      checked4: false,
      checked5: false,
      checked6: true,
      checkList: ['选中且禁用', '复选框 A'],
      checkedCities: ['上海', '北京'],
      checkedCities1: ['上海', '北京'],
      cities: cityOptions,
      isIndeterminate: true,
      checkboxGroup1: ['上海'],
      checkboxGroup2: ['上海'],
      checkboxGroup3: ['上海'],
      checkboxGroup4: ['上海'],
      checkboxGroup5: [],
      checkboxGroup6: [],
    }
  },
  methods: {
    handleCheckAllChange (val) {
      // console.log('val: ', val);
      this.checkedCities = val ? cityOptions : [];
      this.isIndeterminate = false;
    },
    handleCheckedCitiesChange (value) {
      // console.log('value: ', value)
      let checkedCount = value.length
      this.checkAll = checkedCount === this.cities.length;
      this.isIndeterminate = checkedCount > 0 && checkedCount < this.cities.length
    }
  }
}
</script>

<style scoped>
</style>
