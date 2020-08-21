<template>
  <div>
    <b v-bind:style="{ fontSize: fsize + 'px' }" class="text-dark">SOCORZER</b> 
    <h2>Font Size setting</h2>
    <div class="row-12">
    <button @click="upFunction" class="btn btn-outline-danger">+</button>
    <button @click="downFunction" class="btn btn-outline-danger">-</button>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
      fsize:100,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    upFunction: function () {
      this.fsize += 10;
      console.log("fsize = " + this.fsize);
    },
    downFunction: function () {
      this.fsize -= 10;
      console.log(this.fsize);
    },
  },
};
</script>
<style>
</style>