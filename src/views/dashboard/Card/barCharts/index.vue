<template>
  <!-- 容器 -->
  <div class="charts" ref="charts"></div>
</template>

<script>
import * as echarts from "echarts";
export default {
  name: "",
  mounted() {
    // 初始化echarts实例
    let lineCharts = echarts.init(this.$refs.charts);
    // 配置数据
    lineCharts.setOption({
      xAxis: {
        // 隐藏X轴
        show: false,
        // 均分
        type: "category",
      },
      yAxis: {
        show: false,
      },
      // 系列
      series: [
        {
          // 图表形式---柱状图
          type: "bar",
          data: [10, 7, 33, 12, 48, 9,29,10,44,33,22,8],
          color:'cyan'
        },
      ],
      // 布局测试
      grid: {
        left: 0,
        top: 0,
        right: 0,
        bottom: 0,
      },
      tooltip:{}
    });
  },
};
</script>

<style>
.charts {
  width: 100%;
  height: 100%;
}
</style>