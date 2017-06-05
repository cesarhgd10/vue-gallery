<template>
  <div>
    <a @click="emitImage(image)" v-for="image in images" href="#"><div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" :src="image.thumbnail" /></div></a>
  </div>
</template>

<script>
  // import SingleImage from './SingleImage'

  export default {
    props: ['images'],
   // components: {SingleImage},
    methods: {
      emitImage: function (image) {
        this.$emit('emitImage', image)
      }
    }
  }
</script>
