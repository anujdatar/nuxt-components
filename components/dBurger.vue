<template>
  <div class="burger">
    <div class="line1" />
    <div class="line2" />
    <div class="line3" />
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.burger {
  align-self: center;
  cursor: pointer;
  // padding: 10px;
  div .line1, .line2, .line3{
    @include theme-aware('background-color', 'text-main');
    width: 25px;
    height: 3px;
    margin: 5px;
    transition: all 0.3s ease;
  }
  &.toggle .line1 {
    transform: rotate(-45deg) translate(-5px,6px);
  }
  &.toggle .line2 {
      opacity: 0;
  }
  &.toggle .line3 {
      transform: rotate(45deg) translate(-5px,-6px);
  }
}
</style>
