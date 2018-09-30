<template>
  <div class="svg">
    <img v-if="image.length" :src="image">
  </div>
</template>

<script type="text/javascript">
  export default {
    data () {
      return {
      	image: ''
      }
    },
    props: ['type'],
    mounted () {
    	this.image = `https://www.liyu.fun/img/loading/${this.type}.svg`
    }
  }
</script>

<style lang="scss">
  .svg{
    img{
      width: 50px;
    }
  }
</style> 