<template>
  <div class="home">
    <!-- <HelloWorld /> -->
    <XP />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import XP from "@/components/xiaopiao.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    XP
  },
  data(){
    return {
      
    }
  }
};
</script>
