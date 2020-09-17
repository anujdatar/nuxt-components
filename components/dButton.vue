<template>
  <button
    :class="classes"
    @click="$emit('click')"
  >
    {{ buttonText }}
    <d-burger
      :class="burgerToggle"
      :style="{ display: showBurger }"
    />
  </button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: 'Button'
    },
    bg: {
      default: 'primary',
      type: String
    },
    color: {
      default: 'text-white',
      type: String
    },
    large: {
      type: Boolean,
      required: false
    },
    hollow: {
      type: Boolean,
      required: false
    },
    rectangular: {
      type: Boolean,
      required: false
    },
    transparent: {
      type: Boolean,
      required: false
    },
    burger: {
      type: Boolean,
      required: false
    },
    toggle: {
      type: Boolean,
      required: false
    }
  },
  data () {
    return {
      buttonText: this.burger ? '' : this.text,
      showBurger: this.burger ? 'block' : 'none'
    }
  },
  computed: {
    classes () {
      return [
        [this.hollow || this.burger || this.transparent ? '' : this.bg],
        [this.transparent ? '' : this.color],
        {
          hollow: this.hollow,
          large: this.large,
          rectangular: this.rectangular,
          transparent: this.transparent,
          burger: this.burger
        }
      ]
    },
    burgerToggle () {
      return {
        toggle: this.toggle
      }
    }
  }
}
</script>

<style lang="scss">
button {
  text-align: center;
  text-decoration: none;
  display: inline-block;
  cursor: pointer;
  border: none;
  outline: none;
}
button:not(.burger):not(.transparent) {
  font-size: 16px;
  border-radius: 500px;
  padding: 8px 24px;
  margin: 4px 2px;
}
button.hollow {
  border: 2px solid;
  background: transparent !important;
  @include theme-aware-important('color', 'primary')
}
button.burger,
button.transparent {
  background: transparent !important;
  padding: 0;
  // font-size: 24px;
}
button.large:not(.burger) {
  font-size: 24px;
  padding: 10px 30px;
}
</style>
