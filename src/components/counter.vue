<template>
  <div>
    <div class="row-12">
      <button @click="like()" class="btn btn-outline-warning">Like
      </button>
      <button @click="love()" class="btn btn-outline-warning"> Love
      </button>
      <button @click="haha()" class="btn btn-outline-warning"> Haha
      </button>
      <button @click="wow()" class="btn btn-outline-warning">Wow
      </button>
      <button @click="sad()" class="btn btn-outline-warning">Sad
      </button>
      <button @click="angry()" class="btn btn-outline-warning">Angry
      </button>
      <br />
      <br />
      <p v-bind:style="{fontSize: fonts + 'px' }">{{ counter }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
      fonts: 50,
    };
  },
  methods: {
    like: function () {
      this.counter += 1;
      console.log(this.counter);
    },
    love: function () {
      this.counter += 10;
      console.log(this.counter);
    },
    haha: function () {
      this.counter += 5;
      console.log(this.counter);
    },
    wow: function () {
      this.counter += 20;
      console.log(this.counter);
    },
    sad: function () {
      this.counter -= 5;
      console.log(this.counter);
    },
    angry: function () {
      this.counter -= 50;
      console.log(this.counter);
    },
  },
};
</script>


<style>
</style>