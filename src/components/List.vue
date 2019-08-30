<template>
  <div>
      <div class="list-group">
          <Item :deleteInfos="deleteInfos" :key="index" :index="index" :info="info" v-for="(info,index) in infos" class="list-group-item list-group-item-action"/>
      </div>
  </div>
</template>

<script>
import Item from '@/components/Item.vue';
export default {
    props:{
        infos:{
            type: Array
        },
        deleteInfos:Function
    },
    components: {
        Item
    }
}
</script>

<style scoped>

</style>