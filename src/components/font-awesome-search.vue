<template>
  <div>
    <span v-for="(icon, i) in icons" :class="['fa', `fa-${icon.id}`]"></span>
  </div>
</template>

<script>
import icons from '../icons'

export default {

  created () {
    console.log('font-awesome-search created', this.icons)
  },

  data () {
    return {
      icons
    }
  }
}
</script>

<style>
</style>
