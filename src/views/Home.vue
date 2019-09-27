<template>
  <div class="home">
    <HelloWorld :items="items" msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  },
  data(){
    return {
      items:[
        {
          title:"南京油条放心店",
          day:"09-25",
          time:"17:23",
          money:`${Math.floor(Math.random() * 11) + 20}.00`
        }
      ]
    }
  }
};
</script>
