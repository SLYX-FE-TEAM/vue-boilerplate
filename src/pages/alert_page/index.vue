<template>
  <div class="data-container">
    <el-button type="primary" @click="open2">点击打开 Message Box</el-button>

  </div>
</template>

<script>


export default {
    methods: {
        open2() {
            this.$confirm('此操作将永久删除该文件, 是否继续?', '提示', {
                confirmButtonText: '确定',
                cancelButtonText: '取消',
                type: 'warning'
            }).then(() => {
                this.$message({
                    type: 'success',
                    message: '删除成功!'
                });
            }).catch(() => {
                this.$message({
                    type: 'info',
                    message: '已取消删除'
                });
            });
        }
    }
}



</script>

<style lang="sass">
  .data-container
      padding: 30px
      text-align: center
</style>