<template>
  <el-carousel indicator-position="outside">
    <el-carousel-item
      v-for="item in items"
      :key="item"
      v-bind:style="{
        backgroundImage: 'url(' + (item ? item.src : '') + ')',
        backgroundSize: 'contain'
      }"
    >
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      items: [
        { src: "https://ae01.alicdn.com/kf/HTB1P6eASmzqK1RjSZFj762lCFXaG.png" },
        { src: "https://0d077ef9e74d8.cdn.sohucs.com/rmjSFe7_png" },
        { src: "https://0d077ef9e74d8.cdn.sohucs.com/rm1cgpF_png" },
        { src: "https://ae01.alicdn.com/kf/HTB1Ff.Ofe3tHKVjSZSg7604QFXa4.png" }
      ]
    };
  }
};
</script>

<style scoped>
.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
  text-align: center;
}

.el-carousel {
  width: 50%;
}
</style>
