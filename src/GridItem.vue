<template>
  <div id="app">
    <div class="grid-item-container">
      <div class="grid-item-id">
        {{ gridItem.id }}
      </div>
      <div class="grid-item-title">
        {{ gridItem.title }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Grid",
  props: ["gridItem"],
};
</script>

<style scoped>
.grid-item-container {
  border: 1px solid rgb(224, 224, 224);
  width: 60px;
  height: 60px;
  padding: 6px;
  background: rgb(250, 250, 250);
}

.grid-item-id {
  padding-top: 4px;
}

.grid-item-title {
  padding-top: 6px;
  font-size: 12px;
}
</style>