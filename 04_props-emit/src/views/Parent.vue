<template>
  <div class="parent">
      <h1>부모 컴포넌트</h1>
      <!-- 1. prop 이름="내용" -->
      <Child @hungry="parentMsg = '밥먹어라.'" :propFromParent="parentMsg" />
  </div>
</template>

<script>
// 1. import
import Child from '../components/Child.vue'

export default {
    name: 'Parent',
    data () {
        return {
            parentMsg: '부모에서 내리는 메시지'
        }
    },
    // 2. 등록
    components: {
        Child,
    },
}
</script>

<style>
    .parent {
        border: 3px solid red;
        margin: 3px;
        padding: 3px;
    }
</style>