<template>
  <el-row class="demo-autocomplete">
    <el-col :span="12">
      <el-autocomplete
        class="inline-input"
        v-model="state2"
        :fetch-suggestions="querySearch"
        :trigger-on-focus="false"
        @select="handleSelect"
        size="medium"
        suffix-icon="el-icon-search"
      ></el-autocomplete>
    </el-col>
  </el-row>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      restaurants: [],
      state1: "",
      state2: ""
    };
  },
  methods: {
    querySearch(queryString, cb) {
      const restaurants = this.restaurants;
      const results = queryString
        ? restaurants.filter(this.createFilter(queryString))
        : restaurants;
      // 调用 callback 返回建议列表的数据
      cb(results);
    },
    createFilter(queryString) {
      return restaurant => {
        return (
          restaurant.value.toLowerCase().indexOf(queryString.toLowerCase()) ===
          0
        );
      };
    },
    loadAll() {
      return [
        { value: "惊奇队长", address: "长宁区新渔路144号" },
        {
          value: "驯龙高手",
          address: "上海市长宁区淞虹路661号"
        },
        {
          value: "飞驰人生",
          address: "上海市普陀区真北路988号创邑金沙谷6号楼113"
        },
        { value: "权利游戏", address: "天山西路438号" },
        {
          value: "权力游戏",
          address: "上海市长宁区金钟路968号1幢18号楼一层商铺18-101"
        }
      ];
    },
    handleSelect(item) {
      console.log(item);
    }
  },
  mounted() {
    this.restaurants = this.loadAll();
  }
};
</script>

<style scoped>
.demo-autocomplete {
  display: flex;
  justify-content: flex-end;
  height: 80%;
  width: 300px;
}
</style>
