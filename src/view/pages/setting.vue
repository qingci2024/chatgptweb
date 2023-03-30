<template>
  <div class="setting">
    <el-container>
      <el-header>
        <transition name="el-zoom-in-top">
          <div v-show="show" class="transition-box">
            <h3>清辞智能语音聊天系统V1.0</h3>
          </div>
        </transition>
      </el-header>
      <el-main>
        <transition name="el-zoom-in-top">
          <div v-show="show" class="transition-box">
            <span>
              现已接入OpenAI
              如果有什么好的想法提出来
              我们一起来完善这个页面。
            </span>
          </div>
        </transition>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      show: false,
    };
  },
  mounted() {
    this.show = true;
  },
};
</script>

<style>
.transition-box {
  text-align: center;
  margin-top: 5%;
  color: #F2F6FC;
  font-size: 30px;
}

h1 {
  color: aliceblue;
  font-size: 80px;
}

a {
  text-decoration: none;
  color: #67C23A;
}
</style>
