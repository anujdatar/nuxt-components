<template>
  <div class="container">
    <h2>Home Page</h2>
    <div class="test">
      <d-switch />
      <!-- <br> -->
      <d-button text="Lorem" @click="toggleSidebar" />
    </div>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  methods: {
    ...mapMutations(['toggleSidebar']),
    onClick () {
      console.log('aaaaaaaaaaa')
    }
  }
}
</script>

<style lang="scss">
.test {
  display: flex;
}
</style>
