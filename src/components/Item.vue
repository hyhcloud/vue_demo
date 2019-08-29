<template>
  <div>
    <li class="list user">{{common.name}}</li>
    <li class="list common">{{common.comment}}</li>
  </div>
</template>

<script>
export default {
  props: {
    common: {
      type: Object,
    }
  },
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