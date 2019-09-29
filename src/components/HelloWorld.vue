<template>
  <div class="hello">
    <div class="item" v-for="(item, index) in 126" :key="index">
      <div class="item-content">
        <div class="item-content_title">{{shopData[index]}}</div>
        <div class="item-content_time">
          <div class="item-content_day">{{dayData[index]}}</div>
          <div>{{timeData[index]}}</div>
        </div>
      </div>
      <div
        class="item-money"
      >{{`${Math.floor(Math.random() * 11) + 20}.${Math.floor(Math.random() * 40) + 10}`}}</div>
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
    this.dayData = day
    this.timeData =  time,
    this.shopData = shopName
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
