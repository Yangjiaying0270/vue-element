<template>
  <div style="height: 100%;width: 100%">
      <!--主页面-->
      <el-container>
        <!--边栏导航-->
        <el-menu
          router :default-active=this.$route.path  class="el-menu-vertical">  <!--router属性：会将index作为path进行跳转-->
            <el-menu-item  index="/alarm">
              <span slot="title"><i class="iconfont my-eliconclock" style="margin-right: 10px"></i>{{$t('myEventIndex.alarm')}}</span>
            </el-menu-item>
        </el-menu>

        <el-main class="mymain">
          <router-view/>
        </el-main>
      </el-container>

  </div>
</template>

<script>
export default {
  name: 'EventIndex',

}
</script>

<style lang="scss" >
.el-container {
  height:100%;
}
.el-menu-vertical:not(.el-menu--collapse) {
  width: 240px;
  height: 100%;
}
.mymain{
  background-color: white;
}


</style>


