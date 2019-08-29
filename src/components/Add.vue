<template>
  <div>
    <div class="user">
      <label>用户名</label>
      <input v-model="name" type="text" />
    </div>
    <div class="common">
      <h3>评论内容</h3>
      <textarea v-model="comment" class="textarea"></textarea>
    </div>
    <button @click="add">提交</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      common: {
        name: '',
        comment: ''
      }
    }
  },
  methods: {
    
  }
};
</script>

<style scoped>
* {
  margin: 0;
}
div {
  font-size: 14px;
  width: 150px;
  height: 80px;
}
.textarea {
  width: 150px;
  height: 50px;
}
</style>