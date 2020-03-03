<template>
<!--  创建cesium容器-->
    <div id="cesiumContainer" style="width: 100%; height: calc(100%- 47)"></div>
</template>

<script>
// Viewer组件的方式加载
import Viewer from 'cesium/Source/Widgets/Viewer/Viewer'
import buildModuleUrl from 'cesium/Source/Core/buildModuleUrl'// 静态API
import 'cesium/Source/Widgets/widgets.css'
export default {
  name: 'cesiumContainer',
  data () {
    return {
      'viewer': {}
    }
  },
  mounted () {
    // 静态目录
    buildModuleUrl.setBaseUrl('../static/Cesium/')
    // 创建实例

    // .Ion.defaultAccessToken = 'your_access_token'
    this.viewer = new Viewer('cesiumContainer', {
      geocoder: false, // 搜索按钮
      homeButton: false, // 返回初始位置
      navigationHelpButton: false, // 导航帮助按钮，显示默认的地图控制帮助
      fullscreenButton: false, // 全屏显示
      vrButton: false, // vr 模式
      shouldAnimate: false
      // terrainProvider: cesium.createWorldTerrain(), // 添加世界地形
    })
  }

}
</script>

<style>
  .cesium-widget-credits{
    display:none!important;
    visibility:hide!important;
  }

</style>
