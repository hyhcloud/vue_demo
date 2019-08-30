<template>
  <div class="col-4 d-flex align-items-center justify-content-between">
    <div class="form-check">
      <input v-model="choose" type="checkbox" class="form-check-input" />
      <label class="form-check-text">
        已完成
        <span>{{infoCheckedNumber}}</span>/ 全部
        <span>{{infos.length}}</span>
      </label>
    </div>
    <div>
      <button class="btn btn-danger" v-show="infoCheckedNumber" @click="deleteSelected">清除已完成任务</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    infos: Array,
    deleteSelected: Function,
    setAllCompleted: Function
  },
  computed: {
    infoCheckedNumber() {
      return this.infos.filter(info => info.completed).length;
    },
    choose: {
      get() {
        return this.infos.filter(info => info.completed).length === this.infos.length && this.infos.length !== 0;
      },
      set(value) {
        this.setAllCompleted(value);
      }
    }
  }
};
</script>

<style scoped>
</style>