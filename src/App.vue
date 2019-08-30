<template>
  <div class="container" id="app">
    <div class="row flex-column align-items-center">
      <Title :addInfos="addInfos" class="col-4"></Title>
      <List :deleteInfos="deleteInfos" class="col-4" :infos="infos" />
      <Footer />
    </div>
  </div>
</template>

<script>
import Title from "@/components/Title.vue";
import List from "@/components/List.vue";
import Footer from "@/components/Footer.vue";

export default {
  data() {
    return {
      infos: [
        { msg: "a", completed: false },
        { msg: "b", completed: false },
        { msg: "c", completed: true }
      ]
    };
  },
  methods: {
      addInfos(info) {
          this.infos.unshift(info)
      },
      deleteInfos(index){
          this.infos.splice(index,1)
      }
  },
  components: {
    Title,
    List,
    Footer
  }
};
</script>

<style scoped>
</style>
