<template>
  <nav :class="classes">
    <div class="brand">
      <nuxt-link to="/">
        {{ appTitle }}
      </nuxt-link>
    </div>
    <div class="nav-links">
      <ul>
        <li
          v-for="item in routes"
          :key="item.title"
        >
          <nuxt-link
            :to="item.path"
          >
            {{ item.title }}
          </nuxt-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    routes: {
      type: Array,
      required: true
    },
    appTitle: {
      type: String,
      required: true
    },
    elevateOnScroll: {
      type: Boolean,
      required: false
    },
    right: {
      type: Boolean,
      required: false
    }
  },
  computed: {
    classes () {
      return {
        'elevate-on-scroll': this.elevateOnScroll,
        right: this.right
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.onScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.onScroll)
  },
  methods: {
    onScroll (e) {
      const myNav = window.document.querySelector('nav')
      if (window.pageYOffset > 0) {
        myNav.classList.add('is-scrolled')
      } else {
        myNav.classList.remove('is-scrolled')
      }
    }
  }
}
</script>

<style lang="scss" scoped>
nav {
  display: flex;
  width: 100%;
  @include theme-aware('background-color', 'bg-contrast');
  &.sticky {
    position: sticky;
    top: 0;
  }
  &.elevate-on-scroll {
    background-color: transparent;
    position: sticky;
    top: 0;
    &.is-scrolled {
      @include theme-aware-alpha('background', 'bg-contrast', 0.9);
      box-shadow: 0 1px rgba(#7b7b7b, .5);
    }
  }
}
nav .brand {
  font-size: 32px;
  font-weight: bold;
  padding: 10px;
  letter-spacing: 3px;
  a {
    text-decoration: none;
  }
}
nav.right .nav-links {
  margin-left: auto;
}
nav .nav-links {
  display: flex;
  // &.right {
  //   margin-left: auto;
  // }
  ul {
    display: flex;
    justify-content: space-around;
    list-style: none;
    li {
      cursor: pointer;
      display: flex;
      align-items: center;
      &:hover {
        @include theme-aware('background', 'bg-contrast');
        filter: brightness(75%);
      }
    }
    a {
      @include theme-aware('color', 'text-main');
      text-decoration: none;
      font-size: 14px;
      font-weight: 500;
      padding: 0 15px;
      text-transform: uppercase;
      height: 100%;
      display: flex;
      align-items: center;
      &.nuxt-link-exact-active {
        // @include theme-aware-important('color', 'warning');
        @include theme-aware-alpha('background-color', 'warning', 0.3);
        color: color('deep-orange');
      }
    }
  }
}
nav .burger {
  display: none;
  align-self: center;
  cursor: pointer;
  padding: 10px;
  div {
    // @include theme-aware('background-color', 'text-contrast');
    background-color: red;
    width: 25px;
    height: 2px;
    margin: 5px;
    transition: all 0.3s ease;
  }
  &.toggle .line1 {
    transform: rotate(-45deg) translate(-5px,5px);
  }
  &.toggle .line2 {
      opacity: 0;
  }
  &.toggle .line3 {
      transform: rotate(45deg) translate(-5px,-5px);
  }
}

@media screen and (max-width:768px) {
  nav .nav-links {
    display: none;
  }
  nav .burger {
    display: block;
    margin-left: auto;
  }
}
</style>
