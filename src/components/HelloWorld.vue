<template>
  <div class="hello">
    <div class="item" v-for="(item, index) in items" :key="index">
      <div class="item-content">
        <div class="item-content_title">{{shopName[Math.floor((Math.random()*shopName.length))]}}</div>
        <div class="item-content_time">
          <div class="item-content_day">{{item.day}}</div>
          <div >{{`${Math.floor(Math.random() * 2) + 18}:${Math.floor(Math.random() * 41) + 10}`}}</div>
        </div>
      </div>
      <div class="item-money">{{`${Math.floor(Math.random() * 11) + 20}.${Math.floor(Math.random() * 40) + 10}`}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    items: {
      type:Array,
      default:[{}]
    }
  },
  data() {
    return {
      shopName: ["张记手撕烤鸭","觅姐可以喝的麻辣烫","串越舌尖成都冒菜", "鱼小鲜椒麻鱼","杨国福麻辣烫","呱呱叫(秘制)酸菜鱼" ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.item {
  display: flex;
  padding: 0 32px;
  background-image: url("./img/bg.png");
  background-repeat:no-repeat; 
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
