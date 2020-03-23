<template>
  <div class="recommend">
    <div v-for="item in recommends" :key="item.image" class="recommend-item">
      <a :href="item.link"><img :src="item.image" alt=""></a>
      <div>{{item.title}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecommendView",
  props:{
    recommends: {
      type: Array,
      default () {
        return []
      }
    }
  }
}
</script>

<style>
.recommend {
  display: flex;
  width: 100%;
  text-align: center;
  font-size: 14px;

  padding: 15px,0,30px;
  border-bottom: 8px solid #eee;
}
.recommend-item {
  flex:1;

}
.recommend-item img {
  width: 70px;
  height: 70px;
}

</style>