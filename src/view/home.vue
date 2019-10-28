<template>
  <div style="display:flex;flex-direction:column;justify-content:space-between">
    <el-row :gutter="20">
      <el-col :span="8">
        <el-card class="box-card" style="height:250px">
          <div slot="header" class="clearfix">
            <span>快捷入口</span>
            <el-button style="float: right; padding: 3px 0" type="text">编辑</el-button>
          </div>
          <el-row :gutter="20" class="kjrk">
            <el-col :span="8">
              <el-button type="primary">
                <i class="el-icon-edit"></i> 添加用戶
              </el-button>
            </el-col>
            <el-col :span="8">
              <el-button type="success">
                <i class="el-icon-edit"></i> 用户管理
              </el-button>
            </el-col>
            <el-col :span="8">
              <el-button type="warning">
                <i class="el-icon-edit"></i> 帖子管理
              </el-button>
            </el-col>
            <el-col :span="8">
              <el-button type="danger">
                <i class="el-icon-edit"></i> 投诉管理
              </el-button>
            </el-col>
          </el-row>
        </el-card>
      </el-col>
      <el-col :span="8">
        <el-card class="box-card" style="height:250px">
          <div slot="header" class="clearfix">
            <span>数据统计</span>
            <el-button style="float: right; padding: 3px 0" type="text">编辑</el-button>
          </div>
          <el-row :gutter="20" class="sjtj">
            <el-col class="item" :span="12">
              新增用户 /
              <span>15</span>人
            </el-col>
            <el-col class="item" :span="12">
              新增帖子 /
              <span>150</span>条
            </el-col>
            <el-col class="item" :span="12">
              新增充值 /
              <span>1500.00</span>元
            </el-col>
            <el-col class="item" :span="12">
              新增投诉 /
              <span>150</span>条
            </el-col>
          </el-row>
        </el-card>
      </el-col>
      <el-col :span="8">
        <el-card class="box-card" style="height:250px">
          <iframe width="420" scrolling="no" height="60" frameborder="0" allowtransparency="true" src="//i.tianqi.com/index.php?c=code&id=12&icon=1&num=5&site=12"></iframe>
        </el-card>
      </el-col>
    </el-row>
    <div style="height:50px"></div>
    <el-row :gutter="20">
      <el-col :span="8">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span>上周统计</span>
          </div>
          <echartscolumn id="c1" width="400px" height="250px"></echartscolumn>
        </el-card>
      </el-col>
      <el-col :span="8">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span>本周访问量</span>
          </div>
          <echartsline id="c2" width="400px" height="250px"></echartsline>
        </el-card>
      </el-col>
      <el-col :span="8">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span>行业成分</span>
          </div>
          <echartspie id="c3" width="400px" height="250px"></echartspie>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import { echartscolumn, echartsline, echartspie } from "@/components";
export default {
  components: {
    echartscolumn,
    echartsline,
    echartspie
  },
  data(){
    return{
      today: new Date()
    }
  }
};
</script>

<style>
.el-calendar-table .el-calendar-day{
  height: 30px !important;
  width: 30px !important;
  text-align: center;
}
.kjrk button {
  margin: 15px 0;
}
.sjtj .item {
  padding: 20px;
  font-size: 14px;
  display: flex;
  align-item: center;
}
.sjtj .item span {
  color: orangered;
  font-size: 22px;
  padding: 0 10px;
}
</style>