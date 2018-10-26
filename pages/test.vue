<template>
  <div>
    <div class="app"></div>
    <div>
      <p>test</p>
    </div>
  </div>
</template>

<script>



</script>



<style lang="scss">

body {
  padding: 30px;
}

$width: 100px;
$background: #fff;
$background-active: #72d09c;
$border-color: #ddd;
$button-size: 50px;
$button-color: $background;

.toggle {
  width: $width;
  height: $button-size;
  background: $background;
  border: 2px solid $border-color;
  border-radius: 200px;
  padding: 2px;
  transition: background 0.6s;
  
  .draggable {
    width: $button-size;
    height: $button-size;
    background: $button-color;
    border-radius: 100%;
    box-shadow: 0px 3px 10px rgba(0,0,0, 0.6);
    transform: translateX(0%);
    transition: transform 0.05s ease-in-out;
  }
  
  &.active {
    background: $background-active;
    transition: background 0.6s;
  }
}

.app {
  display: flex;
  background-color: #513d56;
}

.switches {
  margin-right: 30px
}

pre {
  margin: 0;
  background: #513d56;
  color: #efefef;
  padding: 20px;
  border-radius: 6px;
  width: 200px;
}
</style>
