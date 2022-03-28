<template>
  <div id="app">
    <img src="./assets/logo.png" />
     <!-- v-action:add -->
    <a-button size="small" type="primary" @click="handleAdd">
      <a-icon type="minus-circle" /> 切换<a-icon type="step-backward" />
    </a-button>
    <!-- <span v-split="['enable', 'forbidden']" class="split-line">AAAAA</span>
    <br />
    <span v-split="['enable', 'forbidden']" class="split-line">BBB</span><br />
    <span v-split="['enable', 'forbidden']" class="split-line">CCCCC</span
    ><br />
    <span v-split="['enable', 'forbidden']" class="split-line">DDDD</span> -->
    <HelloWorld ref="tableAddModal" />
    <hr>
    <TestA></TestA>
    <!-- v-action:add -->
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import TestA from '@/components/TestA'
export default {
  name: "App",
  components: {
    HelloWorld,
    TestA
  },
  methods: {
    handleAdd() {
      console.log(this.$refs.tableAddModal.msg, "AAAAAAAAAAAAAAA");
      this.$refs.tableAddModal.add();
    },
    handleOrgSaveOk(str) {
      alert(str);
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.split-line {
  margin: 0 1px 0 8px;
  display: inline-block;
  height: 0.9em;
  width: 1px;
  vertical-align: middle;
  position: relative;
  top: -0.06em;
  border-left: 1px solid #555;
}
</style>
