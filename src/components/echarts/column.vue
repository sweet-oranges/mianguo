<template>
  <div :id="id" :style="{width,height}">
      
  </div>
</template>

<script>
import echarts from "echarts";
export default {
    props:["width","height","id"],
    mounted(){
        // 基于准备好的dom，初始化echarts实例
    var myChart = echarts.init(document.getElementById(this.id));
    // 绘制图表
    myChart.setOption({
      
      tooltip: {},
      xAxis: {
        data: ["新增用户", "新增帖子", "新增投诉", "新增会员"]
      },
      yAxis: {},
      series: [
        {
          name: "数量",
          type: "bar",
          data: [36, 10, 26, 20]
        }
      ]
    });
    }
}
</script>

<style>

</style>