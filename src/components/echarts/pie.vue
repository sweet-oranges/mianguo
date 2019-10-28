<template>
  <div :id="id" :style="{width,height}"></div>
</template>

<script>
import echarts from "echarts";
export default {
  props: ["width", "height", "id"],
  mounted() {
    // 基于准备好的dom，初始化echarts实例
    var myChart = echarts.init(document.getElementById(this.id));
    

    var option = {
    title : {
        text: '同名数量统计',
        subtext: '纯属虚构',
        x:'center'
    },
    tooltip : {
        trigger: 'item',
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        type: 'scroll',
        orient: 'vertical',
        right: 10,
        top: 20,
        bottom: 20,
        data:['软件互联网','教育','金融','广告媒体','服务'],
        selected: ['a']
    },
    series : [
        {
            name: '行业',
            type: 'pie',
            radius : '55%',
            center: ['40%', '50%'],
            data:  [{value:335, name:'软件互联网'},
                {value:310, name:'教育'},
                {value:234, name:'金融'},
                {value:135, name:'广告媒体'},
                {value:1548, name:'服务'}],
            itemStyle: {
                emphasis: {
                    shadowBlur: 10,
                    shadowOffsetX: 0,
                    shadowColor: 'rgba(0, 0, 0, 0.5)'
                }
            }
        }
    ]
};





    // 绘制图表
    myChart.setOption(option);
  }
};
</script>

<style>
</style>