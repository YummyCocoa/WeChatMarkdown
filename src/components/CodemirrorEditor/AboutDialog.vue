<template>
  <el-dialog
    title="关于"
    class="about__dialog"
    :visible="visible"
    @close="$emit('close')"
    width="30%"
    center
  >
    <div style="text-align: center">
      <h3>一款高度简洁的微信 Markdown 编辑器</h3>
      <p>
        基于项目:
        <a href="https://github.com/doocs/md" target="_blank"
          >WeChat Markdown Editor</a
        >
      </p>
    </div>
    <template slot="footer">
      <el-button
        type="primary"
        @click="onRedirect('https://www.mintimate.cn')"
        plain
      >
        Mintimate's Blog
      </el-button>
      <el-button
        type="primary"
        @click="onRedirect('https://tool.mintimate.cn')"
        plain
      >
        在线工具箱
      </el-button>
    </template>
  </el-dialog>
</template>

<script>
export default {
  props: {
    visible: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    onRedirect(url) {
      window.open(url)
    },
  },
}
</script>

<style lang="less" scoped>
/deep/ .el-dialog {
  min-width: 420px;
}
</style>
