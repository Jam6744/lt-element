## Cell Container 布局列数容器
用于高效快捷搭建详情页面基础结构

### 基础用法
 

:::demo 用于布局页面

```html
<template> 
    <el-cell-container cols='3'>
        <h3>基础信息</h3>
        <el-cell label='姓名姓名：' :value='value' label-width='1'></el-cell>
        
        <el-cell label='年龄：' :value='value' label-width='1' cols='full' full-value-width='9'>
          <template>
            <el-input type="textarea" :rows="3" placeholder="请输入内容" v-model="textarea" size='small'></el-input>
          </template>
        </el-cell>
        <el-cell label='年龄：' :value='value' label-width='1'></el-cell> 
        <el-cell label='年龄：' :value='value' label-width='1'></el-cell>
        <el-cell label='年龄：' :value='value' label-width='1'></el-cell>
    </el-cell-container>
</template>

<script>
  export default {
    data() {
      return {
        value:'dd记对对对对对对对对对对对对对对对对对对对对对对对对对对对对对对对对对对对',
        textarea:'mmm'
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
