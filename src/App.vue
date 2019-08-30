<template>
  <div id="app">
    <Title class="title" />
    <div class="sub">
      <Add :addCommon="addCommon" class="left" />
      <List :common="comment" :deleteCommon="deleteCommon" />
    </div>
  </div>
</template>

<script>
import Title from "@/components/Title.vue";
import Add from "@/components/Add.vue";
import List from "@/components/List.vue";

export default {
  data() {
    return {
      comment: [
        {
          name: "zhangsan",
          comment: "hello"
        },
        {
          name: "lisi",
          comment: "world"
        }
      ]
    };
  },
  components: {
    Title,
    Add,
    List
  },
  methods: {
    addCommon(common) {
      this.comment.unshift(common)
    },
    deleteCommon(index){
      this.comment.splice(index,1)
    }
  }
};
</script>

<style>
.sub {
  display: flex;
  justify-content: center;
}
.left {
  margin-right: 5px;
}
.title {
  height: 300px;
  background-color: #12f832;
  text-align: center;
  line-height: 300px;
}
</style>
