<template>
  <div class="album-info" :release="release" :price="price">More info</div>
</template>

<script>
export default {
  name: 'album-info',
  props: {
    release: {
        type: String,
        default: ''
    },
    price: {
        type: String,
        default: ''
    },
  }
}
</script>

<style scoped lang="scss">
.album-info {}
</style>