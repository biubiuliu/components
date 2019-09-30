<template>
  <div class="home_container">
    <div class="left_box">d</div>
    <el-container>
      <el-header>header</el-header>
      <el-main>
        <canvas-card />
      </el-main>
      <el-footer>footer</el-footer>
    </el-container>
  </div>
</template>
<script>
import canvasCard from '@/components/canvas/canvasCard'
export default {
  components: {
    canvasCard
  },
  data() {
    return {
    }
  }
}
</script>

<style>
.home_container {
  display: flex;
  justify-content: flex-start;
}
.el-header {
  background-color: #b3c0d1;
  color: #333;
  line-height: 60px;
}
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  line-height: 60px;
}
.left_box {
  background: rgb(214, 182, 182);
  width: 20%;
  height: 100vh;
}
</style>
