<template>
  <div class="clearAllContainer">
      <span class="clearAllBtn" v-on:click="clearTodo">Clear All</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      clear: "",
    }
  },
  methods: {
    check() {

    },
    clearTodo: function () {
      // console.log("로컬 초기화")
      this.clear++;
      this.$emit('clearAll', this.clear)
      // console.log("emit clear")
      localStorage.clear();
    }
  }
}
</script>

<style scoped>
.clearAllContainer {
  width: 8.5rem;
  height: 50px;
  line-height: 50px;
  background-color: white;
  border-radius: 5px;
  margin: 0 auto;
}

.clearAllBtn {
  color: #e20303;
  display: block;
}
</style>