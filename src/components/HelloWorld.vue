<template>
  <div class="hello">
    <div class="item" v-for="(item, index) in items" :key="index">
      <div class="item-content">
        <div class="item-content_title">{{item.title}}</div>
        <div class="item-content_time">
          <div class="item-content_day">{{item.day}}</div>
          <div >{{item.time}}</div>
        </div>
      </div>
      <div class="item-money">{{item.money}}</div>
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
  margin-left: 469px;
}
</style>
