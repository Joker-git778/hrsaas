<template>
  <el-card class="page-cools">
    <el-row type="flex" justify="space-between" align="middle">
      <el-col>
        <div v-if="showBefore" class="before">
          <i class="el-icon-info" />
          <!-- 定义前面得插槽 -->
          <slot name="before" />
        </div>
      </el-col>
      <el-col>
        <!-- 后插槽 -->
        <el-row type="flex" justify="end">
          <!-- 定义后面的插槽 -->
          <slot name="after" />
        </el-row>
      </el-col>
    </el-row>
  </el-card>
</template>

<script type="text/ecmascript-6">
export default {
  props: {
    showBefore: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" ref="stylesheet/scss" scoped>
.page-tools {
  margin: 10px 0;
  .before {
    line-height: 34px;
  i {
    margin-right: 5px;
    color: #409eff;
  }
  display: inline-block;
  padding: 0px 10px;
  border-radius: 3px;
  border: 1px solid rgba(145, 213, 255, 1);
  background: rgba(230, 247, 255, 1);
}
}
</style>
