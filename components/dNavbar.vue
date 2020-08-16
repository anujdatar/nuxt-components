<template>
  <nav>
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
    }
  }
}
</script>