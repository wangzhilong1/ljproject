<template>
  <div id="app">
<div id="title-item">
<ul>
  <button>项目</button>
  <button>临建基础</button>
  <button>基础数据</button>
</ul>
</div>
    <div class="title-tool">
      <div class="tool-item">
          <span class="tool-item-name"></span>
      </div>
    </div>
    <router-view/>
 </div>
</template>

<script>
import cesiumViewer from './cesiumViewer'
export default {
  name: 'App',
  comments: {
    'cesiumViewer': cesiumViewer
  }
}
</script>

<style>
html, body ,  #cesiumContainer{
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden;
  }
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 0;
  /*width: 100%;*/
  /*height: 100%;*/
}
  #title-item{
    margin: 0;
    padding: 0;
    width: 100%;
    background: #474747;
    height: 41px;
    min-width: 656px;
    z-index: 10002;

  }
ul {
  display: block;
  list-style-type: disc;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 40px;
  margin: 0;
}
button{

  display:inline;
  float:left;
  font-size: 14px;
  padding: 10px 20px;
  border: 1px;
  color: white;
  border-color: black;
  background: #474747;
  list-style:none;
}
  #title-tool{
    width: 100%;
    height: 96px;
    display: none;
  }
.title-tool {
  width: auto;
  height: 72px;
  position: relative;
  margin: 12px 5px;
  border-right: 2px solid rgba(71, 71, 71, 1);
  padding-right: 25px;
  padding-left: 12px;
  display: flex;
}
  .tool-item{
    width: auto;
    height: 72px;
    position: relative;
    margin: 12px 5px;
    border-right: 2px solid rgba(71, 71, 71, 1);
    padding-right: 25px;
    padding-left: 12px;
    display: flex;

  }
  .tool-item-name{
    display: inline-block;
    min-width: 57px;
    /* padding: 0 5px; */
    height: 18px;
    background: rgba(71, 71, 71, 1);
    border-radius: 3px;
    font-size: 12px;
    /* font-weight: bold; */
    color: rgba(221, 221, 221, 1);
    text-align: center;
    position: absolute;
    left: 16px;
    top: -2px;
  }
</style>
