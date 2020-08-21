<template>
  <div id="app">
    <img class="rounded-circle" src="./assets/scz.png" width="20%" />
    <HelloWorld msg="" />        
    <fontSize />
    <hr />
    <div class="row">
      <div class="col">
        <img class="rounded border border-dark" src="./assets/p1.jpg" width="80%" />
        <br />
        <br />
        <counter />
      </div>
      <div class="col">
        <img class="rounded border border-dark" src="./assets/p2.jpg" width="80%" />
        <br />
        <br />
        <counter />
      </div>
    </div>
    <div class="row">
      <div class="col">

        <hr />
        <div class="row-12">
          ชื่อ-นามสกุล
          <input type="text" v-model="name" />
          รหัส นศ.
          <input type="number" v-model="code" />
          GPA
          <input type="number" v-model="gpa" step="0.1" />
          <br />
          <br /><hr>
        </div>
        <div class="row-12">แสดง:ชื่อ {{name}} รหัส นศ.{{code}} GPA {{gpa}}</div>
        <br />
        <br />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import counter from "./components/counter.vue";
import fontSize from "./components/fontSize.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    counter,
    fontSize,
  },
  data: function () {
    return {
      total: 0,
      name: "",
      code: "",
      gpa: 0.1,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
