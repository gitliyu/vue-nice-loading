<template>
  <transition name="loading-fade">
    <div
            v-show="visible"
            :style="{ backgroundColor: background || '' }"
            class="loading-mask">
      <div class="loading-spinner">
        <spinner :type="type"></spinner>
        <p v-if="text" class="loading-text">{{ text }}</p>
      </div>
    </div>
  </transition>
</template>

<script>
  export default {
    components: {
      Spinner: require('./Spinner.vue').default
    },
    data() {
      return {
        text: null,
        type: null,
        background: null,
        visible: true,
        delay: 0
      };
    }
  };
</script>

<style lang="scss">
  .loading-fade-enter, .loading-fade-leave-to{
    opacity: 0;
  }
  .loading-mask {
    position: absolute;
    z-index: 2000;
    background-color: rgba(0, 0, 0, .8);
    margin: 0;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    -webkit-transition: opacity .5s;
    transition: opacity .5s
  }
  .loading-spinner{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
  }
  .loading-text{
    color: #fff;
  }
</style>
