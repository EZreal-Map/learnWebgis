<template>
  <div id="app">
    <el-container class="app-out-pannel">
      <el-header class="sys-header">一张图项目系统</el-header>
      <el-container class="app-content-pannel">
        <el-aside class="sys-menu">
          <el-menu default-active="1" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose"
            @select="handleMenuSelect" background-color="#545c64" text-color="#fff" active-text-color="#ffd04b"
            :collapse="true">
            <!-- @ === v-on -->
            <el-menu-item index="1">
              <i class="el-icon-monitor"></i>
              <span slot="title">首页大屏</span>
            </el-menu-item>
            <el-menu-item index="2">
              <i class="el-icon-picture-outline"></i>
              <span slot="title">一张图</span>
            </el-menu-item>
          </el-menu>
        </el-aside>
        <el-main class="sys-content">
          <router-view></router-view>
          <!-- <MapView /> -->
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
// import MapView from './components/common/MapView.vue';

export default {
  name: 'App',
  components: {
    // MapView,
  },
  methods: {
    handleMenuSelect(index) {
      if (index === '1') {
        // 跳转到首页大屏
        this.$router.push('/')
      } else if (index === '2') {
        // 跳转一张图
        this.$router.push('/onemap')
      }
    },
  },
};
</script>

<style>
html,
body,
#app {
  position: relative;
  width: 100%;
  height: 100%;
  margin: 0;
}

.app-out-pannel,
.app-content-pannel {
  /* position: relative;
  width: 100px; */
  height: 100%;
  /* margin: 0; */
}

.sys-header {
  background-color: #32373e;
  line-height: 60px;
  color: #fff;
  font-size: 20px;
  font-weight: 700;
}

.app-content-pannel .sys-menu {
  background-color: #545c64;
  width: 64px !important;
  overflow: hidden !important;
}

.app-content-pannel .sys-content {
  padding: 5px;
}
</style>
