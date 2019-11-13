<template>
  <div class="hello">
    <div class="item" v-for="(item, index) in 25" :key="index">
      <div class="item-content">
        <div class="item-content_title">{{shopData[index]}}</div>
        <div class="item-content_time">
          <div class="item-content_day">{{dayData[index]}}</div>
          <div>{{timeData[index]}}</div>
        </div>
      </div>
      <div v-if="shopData[index] ==='鱼小鲜椒麻鱼'" class="item-money">27.80</div>
      <div v-if="shopData[index] ==='呱呱叫(秘制)酸菜鱼'" class="item-money">31.98</div>
      <div v-if="shopData[index] ==='张记手撕烤鸭'" class="item-money">20.8</div>
      <div v-if="shopData[index] ==='喜得美炸鸡汉堡(后宰门店)外卖...'" class="item-money">27.2</div>
      <div v-if="shopData[index] ==='杨国福麻辣烫'" class="item-money">22.90</div>
      <div v-if="shopData[index] ==='觅姐可以喝的麻辣烫'" class="item-money">22.92</div>
      <div v-if="shopData[index] ==='串越舌尖成都冒菜'" class="item-money">24.00</div>
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
    console.log("this.dayData",this.dayData.length);
    
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
.item {
  display: flex;
  padding: 0 32px;
  background-image: url("./img/bg.png");
  background-repeat: no-repeat;
  height: 273px;
  
}
.item-content {
  margin-left: 150px;
  margin-top: 54px;
}
.item-content_title {
  font-size: 40px;
  width: 600px;
  text-align: left;
}
.item-content_time {
  display: flex;
  margin-top: 70px;
  font-size: 36px;
  color: #999999;
}
.item-content_day {
  margin-right: 20px;
}
.item-money {
  margin-top: 42px;
  font-size: 56px;
  margin-left: 155px;
}
</style>
