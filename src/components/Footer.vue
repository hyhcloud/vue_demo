<template>
  <div class="col-4 d-flex align-items-center justify-content-between">
    <div class="form-check">
      <input type="checkbox" class="form-check-input" />
      <label class="form-check-text">
        已完成
        <span>0</span>/ 全部
        <span>2</span>
      </label>
    </div>
    <div>
      <button class="btn btn-danger" @click="deleteSelected">清除已完成任务</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    deleteSelected() {}
  }
};
</script>

<style scoped>
</style>