<template>
  <div id="app">
    <h2 style="padding-left: 20px">Vue draggable grid</h2>
    <grid
      :draggable="true"
      :sortable="true"
      :items="gridItems"
      :height="100"
      :width="100"
    >
      <template slot="cell" scope="props">
        <GridItem :grid-item="props.item" />
      </template>
    </grid>
    <div class="np-credits">wwww.nightprogrammer.com</div>
  </div>
</template>

<script>
import GridItem from "./GridItem";

export default {
  name: "App",
  data() {
    return {
      gridItems: Array(40)
        .fill()
        .map((_, i) => this.createItem(i)),
    };
  },
  components: {
    GridItem,
  },
  methods: {
    createItem(index) {
      const names = ["Gautam", "Tom", "Tim", "Kim", "Lee"];

      return {
        id: index + 1,
        title: names[Math.floor(Math.random() * 5)],
      };
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 24px;
}

.np-credits {
  font-size: 12px;
  margin-top: 40px;
  color: #4b4b4b;
}
</style>