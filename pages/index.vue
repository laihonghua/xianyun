<template>
  <div class="container">
    <!-- 轮播图 -->
    <el-carousel :interval="5000"
                 arrow="always">
      <el-carousel-item v-for="(item,index) in banners"
                        :key="index">
        <div class="banner-image"
             :style="`
                background:url(${item.url}) center center no-repeat;
                background-size:contain contain;
                `">
        </div>
      </el-carousel-item>

    </el-carousel>
  </div>
</template>

<script>


export default {
  data () {
    return {
      // 轮播图数据
      banners: [
        {
          url: "http://157.122.54.189:9095/assets/images/th03.jfif",
        },
        {
          url: "http://157.122.54.189:9095/assets/images/th04.jfif",
        }
      ]
    }
  }

}
</script>

<style scoped lang="less">
.container {
  min-width: 1000px;
  margin: 0 auto;
  position: relative;

  /deep/ .el-carousel__container {
    height: 700px;
  }

  .banner-image {
    width: 100%;
    height: 100%;
  }
}
</style>
