<template>
  <div @mouseenter="itemEnter(true)" @mouseleave="itemEnter(false)">
    <input type="checkbox" v-model="info.completed" class="form-check-input" />
    <label class="form-check-text">{{info.msg}}</label>
    <button @click="deleteInfo()" v-show="isShow" class="ml-5 btn-sm btn-primary">删除</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      bgColor: "white",
      isShow: false
    };
  },
  props: {
    info: {
      type: Object
    },
    index: {
      type: Number
    },
    deleteInfos: Function
  },
  methods: {
    itemEnter(isEnter) {
      // console.log(isEnter);

      if (isEnter) {
        this.bgColor = "#bbb";
        this.isShow = true;
      } else {
        this.bgColor = "white";
        this.isShow = false;
      }
    },
    deleteInfo() {
      if (confirm(`是否删除${this.info.msg}`)) {
        this.deleteInfos(this.index);
      }
    }
  }
};
</script>

<style scoped>
</style>