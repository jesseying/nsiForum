<template>
  <el-scrollbar :height="height" :max-height="height" :native="false">
    <div class="common-layout">
      <el-container>
        <el-header>
          <Header />
        </el-header>
        <el-main>
          <slot />
        </el-main>
        <el-footer class="footer">
          <Footer />
        </el-footer>
      </el-container>
    </div>
  </el-scrollbar>
</template>

<script setup lang="ts">
import Header from './header.vue'
import Footer from './footer.vue'
const height = window.innerHeight
</script>

<style scoped lang="scss">
.layout-container-demo .el-header {
  position: relative;
  background-color: var(--el-color-primary-light-7);
  color: var(--el-text-color-primary);
  line-height: 50px;
}
.layout-container-demo .el-aside {
  color: var(--el-text-color-primary);
  background: var(--el-color-primary-light-8);
}
.layout-container-demo .el-menu {
  border-right: none;
}
.layout-container-demo .el-main {
  padding: 0;
}
.layout-container-demo .toolbar {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  right: 20px;
}
.footer {
  background: var(--el-bg-color);
}
</style>
