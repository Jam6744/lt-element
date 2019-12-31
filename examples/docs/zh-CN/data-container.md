## Data Container 数据容器
用于高效快捷搭建页面基础结构

### 基础用法
 

:::demo 用于查询条件+列表+分页+其它操作按钮

```html
<template> 
    <el-data-container :searchContainer="searchContainer" @search="handleSearch" :operatorContainer="operatorContainer" :tableContainer="tableContainer" :paginationContainer="paginationContainer">
      
    </el-data-container> 
</template>

<script>
  export default {
    data() {
      return {
        searchContainer: {
          isResetAutoSearch: false,
          list: [
            { key: 'name', type: 'input', class: '', placeholder: '姓名', value: '1', fetch: '', cb: '', span: ''},
            { key: 'sex', type: 'select', class: '', placeholder: '请选择', value: '', fetch: '', cb: '', span: '', options: [
              { value: '选项1', label: '黄金糕1' },
              { value: '选项21', label: '黄金糕2' }
            ]},
            { key: 'date', type: 'date', class: '', placeholder: '开始日期', value: '', fetch: '', cb: '', span: ''}
          ]
        },
        operatorContainer: [
          { type: 'primary', text: '新增', cb: this.handleAdd},
          { type: 'primary', text: '删除', cb: this.handleDel}
        ],
        tableContainer: {
          selection:true,
          selectionChange: ()=>{},
          operate: [
            {
              type: 'primary',
              label: '删除',
              cb: this.handleDel
            }
          ],
          head: [
            {
              prop: "moduleCode",
              label: "系统编号"
            },
            {
              prop: "moduleName",
              label: "系统名称"
            }
          ],
          data: [
            {
              moduleCode: '123',
              moduleName: '333'
            },
            {
              moduleCode: '444',
              moduleName: '555'
            }
          ]
        },
        paginationContainer: {
          currentPage: 1,
          total: 1
        }
      }
    },
    methods: {
      handleSearch(parms) {
        console.log('---', parms);
      },
      handleAdd() {
        console.log('新增')
      },
      handleDel(row) {
        console.log('删除', row)
      }
    }
  }
</script>
```
:::
 