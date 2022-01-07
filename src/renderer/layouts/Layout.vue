<script>
import LayoutMenu from "./menu/LayoutMenu.vue";
import LayoutContent from "./content/LayoutContent.vue";
import LatoutFooter from "./footer/LatoutFooter.vue";

export default {
  components: { LayoutMenu, LayoutContent, LatoutFooter },
};
</script>

<template>
  <el-container class="container">
    <el-container>
      <el-aside width="200px">
        <LayoutMenu />
      </el-aside>
      <el-container>
        <el-main>
          <LayoutContent />
        </el-main>
      </el-container>
    </el-container>
    <el-footer>
      <LatoutFooter />
    </el-footer>
  </el-container>
</template>

<style>
.container {
  width: 100%;
  height: 100%;
}
.el-aside {
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-aside::-webkit-scrollbar {
  display: none;
}

.el-main {
  color: #333;
  text-align: center;
  line-height: 160px;
}

.el-footer {
  color: #333;
  text-align: center;
  line-height: 60px;
  padding: 0;
}
</style>
