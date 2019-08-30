<template>
  <div >
    <div class="form-group">
      <input  v-model="queryStr" @keyup.enter="addInfo" class="form-control" type="text" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      queryStr: ""
    };
  },
  props: {
      addInfos: {
          type: Function,
      },
  },
  methods: {
    addInfo() {
        if(!this.queryStr.trim()){
            alert('请输入任务')
            return
        }
        const info = {
            msg: this.queryStr,
            completed: false
        }
        this.addInfos(info)
        this.queryStr = ''
    }
  }
};
</script>

<style>
</style>