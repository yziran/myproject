<!--
 * @Author: ziran.yin ziran.yin@ly.com
 * @Date: 2023-03-19 15:27:04
 * @LastEditors: ziran.yin ziran.yin@ly.com
 * @LastEditTime: 2023-03-19 16:15:04
 * @FilePath: \vue-element-admin\src\views\table\dynamic-table\index.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
  <div class="app-container">
    <div style="margin:0 0 5px 20px">
      固定表头, 按照表头顺序排序
    </div>
    <fixed-thead />

    <div style="margin:30px 0 5px 20px">
      不固定表头, 按照点击顺序排序
    </div>
    <unfixed-thead />
  </div>
</template>

<script>
import FixedThead from './components/FixedThead'
import UnfixedThead from './components/UnfixedThead'

export default {
  name: 'DynamicTable',
  components: { FixedThead, UnfixedThead }
}
</script>

