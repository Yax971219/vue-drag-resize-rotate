<template>
  <div class="view-box">
    <div id="toolbar">Size: {{ width }} x {{ height }}</div>
    <div class="container">
      <div :style="style">
        <vue-drag-resize-rotate :grid="[20,40]" :x="10" :y="20" :maxHeight="290" :maxWidth="290" @resizing="onResizing">
          <p>Grid 20x40 starting with a 10x20 offset and max height, max width values equal to 290.</p>
        </vue-drag-resize-rotate>
      </div>
    </div>
  </div>
</template>

<script>
export default {

  data() {
    return {
      width: 200,
      height: 200,
      style: {
        position: 'relative',
        height: '100%',
        backgroundColor: '#808080',
        background: 'linear-gradient(-90deg, rgba(0, 0, 0, .1) 1px, transparent 1px), linear-gradient(rgba(0, 0, 0, .1) 1px, transparent 1px)',
        backgroundSize: '20px 40px, 20px 40px',
        backgroundPosition: '10px 20px'
      }
    }
  },
  methods: {
    onResizing(x, y, width, height) {
      this.width = width
      this.height = height
    }
  }
}
</script>

<style>
</style>