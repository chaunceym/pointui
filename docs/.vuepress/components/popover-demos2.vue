<template>
  <div>
    <p-popover position="right" trigger="hover">
      <template style="z-index: 999"slot="content">
        <div>响应</div>
      </template>
      <p-button>按钮</p-button>
    </p-popover>
    <p-popover trigger="hover">
      <template slot="content">
        <div >响应</div>
      </template>
      <p-button>按钮</p-button>
    </p-popover>
    <p-popover position="bottom" trigger="hover">
      <template slot="content">
        <div >响应</div>
      </template>
      <p-button>按钮</p-button>
    </p-popover>
    <p-popover position="left" trigger="hover">
      <template slot="content">
        <div >响应</div>
      </template>
      <p-button>按钮</p-button>
    </p-popover>
  </div>
</template>
<script>
  import Popover from '../../../src/Popover'
  import Button from '../../../src/Button'
  export default {
    components:{
      'p-popover': Popover,
      'p-button': Button,
    },
  }
</script>
<style scoped lang="scss">
</style>