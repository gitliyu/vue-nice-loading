<template>
  <div class="svg">
    <img v-if="showSvg('audio')" src="../assets/images/audio.svg">
    <img v-else-if="showSvg('ball-triangle')" src="../assets/images/ball-triangle.svg">
    <img v-else-if="showSvg('bars')" src="../assets/images/bars.svg">
    <img v-else-if="showSvg('circles')" src="../assets/images/circles.svg">
    <img v-else-if="showSvg('grid')" src="../assets/images/grid.svg">
    <img v-else-if="showSvg('hearts')" src="../assets/images/hearts.svg">
    <img v-else-if="showSvg('oval')" src="../assets/images/oval.svg">
    <img v-else-if="showSvg('puff')" src="../assets/images/puff.svg">
    <img v-else-if="showSvg('rings')" src="../assets/images/rings.svg">
    <img v-else-if="showSvg('spinning-circles')" src="../assets/images/spinning-circles.svg">
    <img v-else-if="showSvg('tail-spin')" src="../assets/images/tail-spin.svg">
    <img src="../assets/images/three-dots.svg" v-else>
  </div>
</template>

<script type="text/javascript">
  export default {
    data () {
      return {}
    },
    props: ['type'],
    methods: {
      showSvg (type) {
        return this.type === type;
      }
    }
  }
</script>