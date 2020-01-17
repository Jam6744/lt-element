## Cell Container 布局列数容器
用于高效快捷搭建详情页面基础结构

### 基础用法
 

:::demo 用于布局页面

```html 
<template>  
    <el-cell-container cols='2'>
        <h3>基础信息</h3> 
        <el-cell label='工作单位' :value='value'></el-cell>
        <el-cell label='工作单位及所在部门' :value='value' label-width='3'></el-cell>
        <el-cell label='部门名称' :value='value'></el-cell>
        <el-cell label='年龄' :value='value'></el-cell>
        <el-cell label='备注信息' :value='value' cols="full">
          <template>
              <el-input  v-model='value' placeholder='请输入内容' size='small'></el-input>
          </template>
        </el-cell>
    </el-cell-container>
</template>
 
<script>
  export default {
    data() {
      return {
        value:'软件产业基地' 
      }
    },
    methods: {
      
    }
  }
</script>
```
:::
  
### Attributes
| 参数      | 说明          | 类型      | 可选值                           | 默认值  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| cols      | 分成多少列     | string | 1/2/3/4/5/6 | 1 |
