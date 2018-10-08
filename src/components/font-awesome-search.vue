<template>
  <div class="font-awesome-search">
    <el-button v-for="icon in icons" :key="icon.id" @click="click(icon)">
      <span :class="['icon', 'fa', `fa-${icon.id}`]"></span>
      <span>{{icon.name}}</span>
    </el-button>
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
  },

  methods: {
    click (icon) {
      this.$emit('icon-select', icon)
    }
  }
}
</script>

<style>
.font-awesome-search .icon{
  margin-right: 4px;
}
</style>
