<template>
  <aside
    class="side-nav"
    :class="isSidebarOpen ? onOpen : ''"
  >
    <div class="header">
      <div class="brand">
        {{ appTitle }}
      </div>
      <d-button burger toggle @click="toggleSidebar" />
    </div>
    <hr>
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
  </aside>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  props: {
    appTitle: {
      type: String,
      required: true
    },
    routes: {
      type: Array,
      required: true
    },
    right: {
      type: Boolean,
      required: false
    }
  },
  computed: {
    isSidebarOpen () {
      return this.$store.state.sidebarOpen
    },
    onOpen () {
      return 'is-open'
    }
  },
  methods: mapMutations(['toggleSidebar'])
}
</script>

<style lang="scss" scoped>
aside.side-nav {
  position: fixed;
  top: 0;
  right: -50px;
  height: 100vh;
  width: 0;
  z-index: 1;
  @include theme-aware('background-color', 'bg-main');
  transition: 0.3s;
  display: flex;
  flex-direction: column;
}
aside.side-nav.is-open {
  right: 0;
  width: 50%;
  overflow: hidden;
}

aside.side-nav .header {
  display: flex;
  width: 100%;
  .brand {
    font-size: 32px;
    font-weight: bold;
    padding: 10px;
    letter-spacing: 3px;
  }
}
aside.side-nav .nav-links ul {
  z-index: -1;
  list-style: none;
  padding-left: 0;
  height: 80%;
  li {
    height: 100%;
    &:hover {
      @include theme-aware('background', 'bg-contrast');
      filter: brightness(75%);
    }
    a {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;

      @include theme-aware('color', 'text-main');
      text-decoration: none;
      font-size: 1.1rem;
      text-transform: uppercase;
      font-weight: bold;

      &.nuxt-link-exact-active {
        background-color: rgba(color('orange'), 0.2);
        color: color('deep-orange');
      }
    }
  }
}

// @media screen and (min-width:768px) {
//   aside.side-nav {
//     display: none;
//   }
// }
</style>
