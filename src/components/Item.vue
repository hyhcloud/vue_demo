<template>
  <div>
    <li class="list user">
      {{common.name}}
      <button @click="deleteItem">删除</button>
    </li>
    <li class="list common">
      {{common.comment}}
      <button @click="deleteItem">删除</button>
    </li>
  </div>
</template>

<script>
export default {
  props: {
    common: {
      type: Object
    },
    index: {
      type: Number
    },
    deleteCommon: Function
  },
  methods: {
    deleteItem() {
      const { index, deleteCommon } = this;
      deleteCommon(index);
    }
  }
};
</script>

<style scoped>
.list {
  height: 30px;
  width: 600px;
  border: 1px solid #bbb;
}
.common {
  line-height: 25px;
}
</style>