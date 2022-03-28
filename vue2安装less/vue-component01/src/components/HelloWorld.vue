<template>
  <div v-if="visible" class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>

    <a-button @click="handleOrgSaveOk">子按钮</a-button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      visible: false,
    };
  },
  methods: {
    add() {
      this.visible = !this.visible;
    },
    handleOrgSaveOk() {
      this.$parent.handleOrgSaveOk("来自子组件的参数");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
