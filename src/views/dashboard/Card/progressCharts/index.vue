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
        // 最小值和最大值的设置
        min:0,
        max:100
      },
      yAxis: {
        show: false,
        // 均分
        type: "category",
      },
      // 系列
      series: [
        {
          // 图表形式---柱状图
          type: "bar",
          data: [78],
          color:'cyan',
          // 柱状图的宽度设置
          barWidth:10,
          color:'green',
          // 背景颜色
          showBackground:true,
          // 设置背景颜色
          backgroundStyle:{
            color:'#eee',
          },
          // 文本
          label:{
            show:true,
            // 改变文本内容
            formatter:'|',
            // 文本标签位置调试
            position:'right',
          }
        },
      ],
      // 布局测试
      grid: {
        left: 0,
        top: 0,
        right: 0,
        bottom: 0,
      },
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