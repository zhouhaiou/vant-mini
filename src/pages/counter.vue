<template>
  <div class="counter-warp">
    <p>Vuex counter：{{ count }}</p>
    <p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </p>

    <a href="/pages/index" class="home">去往首页</a>
  </div>
</template>

<script>
import { mapState, mapMutations, mapGetters } from "vuex";
export default {
  config: {
    navigationBarTitleText: "Vuex示例",
    navigationBarBackgroundColor: "#f40"
  },

  computed: {
    ...mapGetters(["count"])
  },

  methods: {
    ...mapMutations(["increment", "decrement"])
  }
};
</script>

<style lang="scss">
.counter-warp {
  text-align: center;
  margin-top: 100px;
  .home {
    display: inline-block;
    margin: 100px auto;
    padding: 5px 10px;
    color: blue;
    border: 1px solid blue;
  }
}
</style>
