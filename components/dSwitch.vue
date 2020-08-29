<template>
  <label
    class="switch"
    :class="classes"
  >
    <input v-model="isActive" type="checkbox">
    <span class="track" :class="isActive ? onClass : ''" />
    <span
      class="thumb"
      :class="[isActive ? onClass : '', hover ? onClass : '']"
      @mouseover="hover = true"
      @mouseleave="hover = false"
    />
  </label>
</template>

<script>
export default {
  props: {
    inset: {
      type: Boolean,
      required: false
    },
    square: {
      type: Boolean,
      required: false
    },
    icon: {
      default: '',
      type: String,
      required: false
    },
    color: {
      default: 'primary',
      type: String
    }
  },
  data () {
    return {
      isActive: false,
      hover: false
    }
  },
  computed: {
    classes () {
      return {
        inset: this.inset,
        square: this.square
      }
    },
    onClass () {
      return this.color
    }
  }
}
</script>

<style lang="scss" scoped>
$width: 52px;
$height: 26px;
$track-height: 12px;
$thumb: 20px;
// swith outer element -> label
.switch {
  width: $width;
  height: $height;
  display: inline-block;
  position: relative;
}
// switch input checkbox element
.switch > input {
  height: 0;
  width: 0;
  visibility: hidden;
}
// switch slider track -> span
.switch > .track {
  cursor: pointer;
  background-color: black;
  opacity: 0.3;

  position: absolute;
  top: calc(50% - #{$track-height / 2});
  left: 3px;

  height: $track-height;
  width: $width - 6px;
  border-radius: $track-height / 2;
  -webkit-transition: 0.3s;
  transition: 0.3s;
}
// switch thumb element -> span
.switch > .thumb {
  cursor: pointer;
  background-color: white;

  position: absolute;
  top: calc(50% - #{$thumb / 2});
  left: 0;

  display: flex;
  justify-content: center;
  align-items: center;

  height: $thumb;
  width: $thumb;
  border-radius: $thumb / 2;
  -webkit-transition: 0.3s;
  transition: 0.3s;
}
// change color when input is checked
// .switch > .thumb:hover,
// .switch > input:checked ~ .thumb,
// .switch > input:checked + .track {
//   background-color: var(--active-color);
// }
// move switch thumb/knob on click
.switch > input:checked ~ .thumb {
  left: calc(100% - 3px);
  -webkit-transform: translateX(-100%);
  -ms-transform: translateX(-100%);
  transform: translateX(-100%);
}
.switch.inset > input ~ .thumb:active {
  width: $width - 6px;
}
// switch variations
.switch.inset > .track {
  top: 0;
  left: 0;

  height: $height;
  width: $width;
  border-radius: $height / 2;
}
.switch.inset > .thumb {
  left: 3px;
}
.switch:not(.inset):not(.flat) > .thumb {
  box-shadow: 0 2px 4px -1px rgba(0,0,0,.2) , 0 4px 5px 0 rgba(0,0,0,.14), 0 1px 10px 0 rgba(0,0,0,.12);
}
.switch.square > .track,
.switch.square > .thumb,
.switch.inset.square > .track,
.switch.inset.square > .thumb {
  border-radius: 0;
}
</style>
