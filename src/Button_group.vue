<template>
  <div class="g-button-group">
    <slot/>
  </div>
</template>

<script >
  export default {
    name: 'PointButtonGroup',
    mounted() {
      for(let node of this.$el.children){
        let name = node.nodeName
        if(name !== 'BUTTON'){
          console.warn(`g-button-group里的元素必须是button,而你的是${name}`)
        }
      }
    }
  }
</script>

<style lang="scss" scoped>
  $border-radius: 4px;
.g-button-group{
  display: inline-flex;
  vertical-align: middle;
  > .g-button{
    border-radius: 0;
    &:not(:first-child){
      margin-left: -1px;
    }
    &:first-child{
      border-top-left-radius: $border-radius;
      border-bottom-left-radius: $border-radius;
    }
    &:last-child{
      border-top-right-radius: $border-radius;
      border-bottom-right-radius: $border-radius;
    }
    &:hover{
      position: relative;
      z-index: 1;
    }
  }
}
</style>