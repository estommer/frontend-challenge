<template>
  <div class="album-info">
    <div v-if="isInfoShown" class="album-info__text">
      <p>Release: {{release}}</p>
      <p>Price: {{price}}</p>
    </div>
    <button class="album-info__btn" @click="toggleInfo">{{isInfoShown ? 'Less' : 'More'}} info</button>
  </div>
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
  },
  data() {
    return {
      isInfoShown: false
    }
  },
  methods: {
    toggleInfo() {
      this.isInfoShown = !this.isInfoShown;
    }
  }
}
</script>

<style scoped lang="scss">
.album-info {
  &__text {
    font-weight: 500;
  }

  &__btn {
    width: 140px;
    border: none;
    border-radius: 20px;
    background: linear-gradient(137deg, #b9e796 0%, #ffa541 100%);
    transition: background 0.1s ease-out;
    color: white;
    padding: 10px 20px;
    font-weight: 600;
    font-size: 20px;
    cursor: pointer;

    &:hover {}

    &:active {}

  }
}
</style>