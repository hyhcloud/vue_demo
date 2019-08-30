<template>
  <div>
    <h3>评论回复</h3>
    <ul>
      <Item :deleteCommon="deleteCommon" :index="index" v-for="(item,index) in common" :key="index" :common="item" />
    </ul>
  </div>
</template>

<script>
import Item from "@/components/Item.vue";
export default {
  props: {
    common: Array,
    deleteCommon: Function
  },
  components: {
    Item
  },
};
</script>

<style scoped>
div {
  width: 600px;
}
.user {
  height: 25px;
  line-height: 25px;
}
</style>