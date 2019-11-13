<template>
  <div class="hello">
    <div class="item" v-for="(item, index) in 25" :key="index">
      <div class="item-content">
        <div>{{`**********#${Math.floor(Math.random() * 11) + 20}饿了么***********`}}</div>
        <div class="item-content_title">{{shopData[index]}}</div>
        <div>—— —— 已在线支付 —— ——</div>
        <div class="item-content_time">
          <div class="item-content_day">{{dayData[index]}}</div>
          <div>{{timeData[index]}}</div>
        </div>
        <div v-if="shopData[index] ==='鱼小鲜椒麻鱼'">
          <div class="shop-item-tips">------------------1号篮子------------------</div>
          <div class="shop-item-caijia">
            <div>激情椒麻鱼(单人餐含4个配菜+1份米饭)-龙利鱼[微辣]</div>
            <div>X1 39.80</div>
          </div>
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
        <div v-if="shopData[index] ==='呱呱叫(秘制)酸菜鱼'">
          <div class="shop-item-tips">------------------1号篮子------------------</div>
           <div class="shop-item-caijia">
            <div>藤椒鱼(2人套餐)</div>
            <div>X1 55.98</div>
          </div>
          <div class="shop-item-tips">------------------其他费用------------------</div>
          <div class="shop-item-other"> 
            <div>餐盒</div>
            <div>{{`X1 3.00`}}</div>
          </div>
          <div class="shop-item-other"> 
            <div>蜂鸟转送</div>
            <div>{{`X1 0`}}</div>
          </div>
          <div class="shop-item-other">
            <div>店铺满减优惠</div>
            <div>{{`-22.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>品质联盟专享红包</div>
            <div>{{`-5.00`}}</div>
          </div>
          <div class="shop-item-money">
            <div>实付</div>
            <div>{{`31.98`}}</div>
          </div>
        </div>
        <div v-if="shopData[index] ==='张记手撕烤鸭'">
          <div class="shop-item-tips">------------------1号篮子------------------</div>
           <div class="shop-item-caijia">
            <div>精品烤鸭套餐饭(推荐)</div>
            <div>X1 35.80</div>
          </div>
          <div class="shop-item-tips">------------------其他费用------------------</div>
          <div class="shop-item-other"> 
            <div>餐盒</div>
            <div>{{`X1 2.00`}}</div>
          </div>
          <div class="shop-item-other"> 
            <div>蜂鸟转送</div>
            <div>{{`X1 0`}}</div>
          </div>
          <div class="shop-item-other">
            <div>店铺满减优惠</div>
            <div>{{`-12.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>品质联盟专享红包</div>
            <div>{{`-5.00`}}</div>
          </div>
          <div class="shop-item-money">
            <div>实付</div>
            <div>{{`20.8`}}</div>
          </div>
        </div>
        <div v-if="shopData[index] ==='喜得美炸鸡汉堡(后宰门店)外卖...'">
          <div class="shop-item-tips">------------------1号篮子------------------</div>
           <div class="shop-item-caijia">
            <div>一盒子大鸡排-孜然+辣椒</div>
            <div>X1 17.90</div>
          </div>
          <div class="shop-item-caijia">
            <div>藤椒鸡腿堡</div>
            <div>X1 15.90</div>
          </div>
          <div class="shop-item-caijia">
            <div>香辣鸡腿堡</div>
            <div>X1 15.90</div>
          </div>
          <div class="shop-item-tips">------------------其他费用------------------</div>
          <div class="shop-item-other"> 
            <div>餐盒</div>
            <div>{{`X1 2.00`}}</div>
          </div>
          <div class="shop-item-other"> 
            <div>蜂鸟转送</div>
            <div>{{`X1 0.5`}}</div>
          </div>
          <div class="shop-item-other">
            <div>店铺满减优惠</div>
            <div>{{`-20.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>品质联盟专享红包</div>
            <div>{{`-5.00`}}</div>
          </div>
          <div class="shop-item-money">
            <div>实付</div>
            <div>{{`27.2`}}</div>
          </div>
        </div>
        <div v-if="shopData[index] ==='杨国福麻辣烫'">
          <div class="shop-item-tips">------------------1号篮子------------------</div>
          <div class="shop-item-caijia">
            <div>娃娃菜</div>
            <div>X2 5.60</div>
          </div>
          <div class="shop-item-caijia">
            <div>海带结</div>
            <div>X1 3.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>笋尖</div>
            <div>X2 5.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>生菜</div>
            <div>X1 2.50</div>
          </div>
          <div class="shop-item-caijia">
            <div>藕片</div>
            <div>X1 2.50</div>
          </div>
          <div class="shop-item-caijia">
            <div>笋片</div>
           <div>X1 2.50</div>
          </div>
          <div class="shop-item-caijia">
            <div>中麻中辣</div>
           <div>X1 0.20</div>
          </div>
          <div class="shop-item-caijia">
            <div>莴笋</div>
           <div>X1 2.50</div>
          </div>
          <div class="shop-item-caijia">
            <div>手擀面</div>
           <div>X1 3.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>鹌鹑蛋</div>
           <div>X2 7.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>蒜蓉</div>
           <div>X2 0.80</div>
          </div>
          <div class="shop-item-tips">------------------其他费用------------------</div>
          <div class="shop-item-other"> 
            <div>餐盒</div>
            <div>{{`X1 2.00`}}</div>
          </div>
          <div class="shop-item-other"> 
            <div>蜂鸟转送</div>
            <div>{{`3.50`}}</div>
          </div>
          <div class="shop-item-other">
            <div>店铺满减优惠</div>
            <div>{{`-18.00`}}</div>
          </div>
          <div class="shop-item-money">
            <div>实付</div>
            <div>{{`22.90`}}</div>
          </div>
        </div>
        <div v-if="shopData[index] ==='觅姐可以喝的麻辣烫'">
          <div class="shop-item-tips">------------------1号篮子------------------</div>
          <div class="shop-item-caijia">
            <div>微辣骨汤煮</div>
            <div>X1 1.58</div>
          </div>
          <div class="shop-item-caijia">
            <div>娃娃菜</div>
            <div>X1 2.98</div>
          </div>
          <div class="shop-item-caijia">
            <div>金针菇</div>
            <div>X1 3.58</div>
          </div>
          <div class="shop-item-caijia">
            <div>笋尖</div>
            <div>X2 5.96</div>
          </div>
          <div class="shop-item-caijia">
            <div>生菜</div>
            <div>X1 2.98</div>
          </div>
          <div class="shop-item-caijia">
            <div>花菜</div>
           <div>X1 3.98</div>
          </div>
          <div class="shop-item-caijia">
            <div>莴笋</div>
           <div>X2 5.96</div>
          </div>
          <div class="shop-item-caijia">
            <div>鹌鹑蛋</div>
           <div>X3 8.94</div>
          </div>
          <div class="shop-item-caijia">
            <div>方便面</div>
           <div>X2 7.96</div>
          </div>
          <div class="shop-item-tips">------------------其他费用------------------</div>
          <div class="shop-item-other"> 
            <div>餐盒</div>
            <div>{{`X1 2.50`}}</div>
          </div>
          <div class="shop-item-other"> 
            <div>蜂鸟转送</div>
            <div>{{`0.50`}}</div>
          </div>
          <div class="shop-item-other">
            <div>店铺满减优惠</div>
            <div>{{`-18.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>觅姐麻辣烫(全国)专享红包</div>
            <div>{{`-6.00`}}</div>
          </div>
          <div class="shop-item-money">
            <div>实付</div>
            <div>{{`22.92`}}</div>
          </div>
        </div>
        <div v-if="shopData[index] ==='串越舌尖成都冒菜'">
          <div class="shop-item-tips">------------------1号篮子------------------</div>
          <div class="shop-item-caijia">
            <div>培根+包心鱼丸+鹌鹑蛋+丸子+实数</div>
            <div>X1 42.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>生菜</div>
            <div>X1 4.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>竹笋</div>
            <div>X1 4.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>莴笋</div>
            <div>X1 4.00</div>
          </div>
          <div class="shop-item-caijia">
            <div>微麻加辣</div>
            <div>X1 2.00</div>
          </div>
          <div class="shop-item-tips">------------------其他费用------------------</div>
          <div class="shop-item-other"> 
            <div>餐盒</div>
            <div>{{`X1 1.00`}}</div>
          </div>
          <div class="shop-item-other"> 
            <div>蜂鸟转送</div>
            <div>{{`0.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>店铺满减优惠</div>
            <div>{{`-28.00`}}</div>
          </div>
          <div class="shop-item-other">
            <div>品质联盟专享红包</div>
            <div>{{`-5.00`}}</div>
          </div>
          <div class="shop-item-money">
            <div>实付</div>
            <div>{{`24.00`}}</div>
          </div>
        </div>
        <div class="shop-item-tips">------------------------------------</div>
        <div class="shop-user-info">珠江路600号谷阳世纪大厦1407</div>
        <div class="shop-user-info">程**</div>
        <div class="shop-user-info">[超级会员]</div>
        <div class="shop-user-info">17512586076</div>
        <div class="shop-line">{{`**********饿了么**********`}}</div>
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
  width: 230px;
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
  width: 220px;
}
.shop-item-money {
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 24px;
  margin-top: 8px;
  width: 220px;
}
.shop-user-info {
  font-size: 24px;
  margin-top: 8px;
  width: 220px;
}
.shop-line {
  margin-top: 32px;
}
.shop-item-caijia {
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 18px;
  width: 220px;
}
</style>
