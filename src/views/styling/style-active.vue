<template>
  <div class="view-box">
    <div id="toolbar">活动状态下具有自定义类名的组件</div>
    <div class="container">
      <vue-drag-resize-rotate class-name-active="my-active-class" class-name="my-class">
        <p>
          You can provide a default class name for the component when it's active using the
          <b>class-name-active</b> prop.
        </p>
      </vue-drag-resize-rotate>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.my-class {
  border: 1px solid red;
  -webkit-transition: background-color 200ms linear;
  -ms-transition: background-color 200ms linear;
  transition: background-color 200ms linear;
}
.my-active-class {
  border: 1px solid black;
  -webkit-box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.75);
  box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.75);
}
</style>