<template>
  <div class="view-box">
    <div id="toolbar">
      <label>
        <input type="checkbox" v-model="x" /> X
      </label>
      <label>
        <input type="checkbox" v-model="y" /> Y
      </label>
    </div>
    <div class="container">
      <vue-drag-resize-rotate :axis="axis">
        <p>Draggable on {{ axis }} axis.</p>
      </vue-drag-resize-rotate>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      x: true,
      y: true
    }
  },
  computed: {
    axis() {
      if (this.x && this.y) return 'both'

      if (this.x) return 'x'

      if (this.y) return 'y'

      return false
    }
  }
}
</script>

<style>
</style>