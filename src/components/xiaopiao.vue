<template>
  <div class="hello">
    <div class="item" v-for="(item, index) in 126" :key="index">
      <div class="item-content">
        <div>{{`******************#${Math.floor(Math.random() * 11) + 20}饿了么******************`}}</div>
        <div class="item-content_title">{{shopData[index]}}</div>
        <div>—— —— 已在线支付 —— ——</div>
        <div class="item-content_time">
          <div class="item-content_day">{{dayData[index]}}</div>
          <div>{{timeData[index]}}</div>
        </div>
        <div>
          <div class="shop-item-tips">------------------1号篮子------------------</div>
          <div class="shop-item-title">{{`激情椒麻鱼(单人餐含4个配菜+1份米饭)-龙利鱼[微辣] X1 39.80`}}</div>
          <div class="shop-item-tips">------------------其他费用------------------</div>
          <div class="shop-item-other"> 
            <div>餐盒</div>
            <div>{{`X1 2.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>店铺满减优惠</div>
            <div>{{`-9.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>品质联盟专享红包</div>
            <div>{{`-5.00`}}</div>
          </div>
          <div class="shop-item-money">
            <div>实付</div>
            <div>{{`27.80`}}</div>
          </div>
        </div>
        <div class="shop-item-tips">------------------------------------</div>
        <div class="shop-user-info">珠江路600号谷阳世纪大厦1407</div>
        <div class="shop-user-info">程**</div>
        <div class="shop-user-info">[超级会员]</div>
        <div class="shop-user-info">17512586076</div>
        <div class="shop-line">{{`******************饿了么******************`}}</div>
      </div>
    </div>
  </div>
</template>

<script>
import { day, time, shopName } from "./time.js";
export default {
  name: "HelloWorld",
  data() {
    return {
      dayData: [],
      timeData: [],
      shopData: []
    };
  },

  created() {
    this.dayData = day;
    (this.timeData = time), (this.shopData = shopName);
    // let dd= [];
    // for (let index = 0; index < 130; index++) {
    //   // const element = this.rendomtime();
    //   // const element = this.shopName[Math.floor((Math.random()* this.shopName.length))]
    //   const element = `${Math.floor(Math.random() * 11) + 20}.${Math.floor(Math.random() * 40) + 10}`
    //   dd.push(element)
    // }
    // console.log(this.shopData)
  },

  methods: {
    rendomtime() {
      return `${Math.floor(Math.random() * 2) + 18}:${Math.floor(
        Math.random() * 31
      ) + 10}`;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.item-content {
  width: 500px;
  margin-top: 100px;
}
.item-content_time {
  display: flex;
}
.item-content_day {
  margin-right: 16px;
}
.shop-item-title {
  font-size: 18px;
}
.shop-item-tips {
  font-size: 14px;
}
.shop-item-other {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.shop-item-money {
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 24px;
  margin-top: 8px;
}
.shop-user-info {
  font-size: 24px;
  margin-top: 8px;
}
.shop-line {
  margin-top: 32px;
}
</style>
