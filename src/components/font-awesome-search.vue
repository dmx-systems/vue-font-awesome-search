<template>
  <div class="font-awesome-search">
    <el-button v-for="icon in icons" :class="['fa', `fa-${icon.id}`]" :title="icon.name" :key="icon.id"
      @click="click(icon)">
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
.font-awesome-search .el-button {
  font-size: 24px !important;
  color: var(--color-topic-icon);
  margin-left: 0;
  margin-right: 3px;
  margin-bottom: 3px;
}
</style>
