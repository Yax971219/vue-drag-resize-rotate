<template>
  <div class="view-box">
    <div id="toolbar">
      X:
      <input type="number" v-model.number="x" />
      Y:
      <input type="number" v-model.number="y" />
      Width:
      <input type="number" v-model.number="w" />
      Height:
      <input type="number" v-model.number="h" />
    </div>
    <div class="container">
      <vue-drag-resize-rotate :x="x" :y="y" :w="w" :h="h" @resizing="onResize" @dragging="onDrag">
        <p>Basic controlled component.</p>
      </vue-drag-resize-rotate>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      x: 0,
      y: 0,
      w: 100,
      h: 100
    }
  },
  methods: {
    onDrag(left, top) {
      this.x = left
      this.y = top
    },
    onResize(left, top, width, height) {
      this.x = left
      this.y = top
      this.w = width
      this.h = height
    }
  }
}
</script>

<style>
</style>