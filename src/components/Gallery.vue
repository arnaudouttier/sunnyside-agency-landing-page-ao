<template>
    <div class="gallery">
        <img  
            v-for="image in images" v-bind:key="image.id" 
            :srcset="image.urldesktop + ' 600w, '"
            :src="image.urlmobile" 
            :alt="image.alt">
    </div>
</template>

<script>
export default {
  data () {
      return {
          images : [
                
                { id:1, urlmobile : require('../assets/images/mobile/image-gallery-milkbottles.jpg')  , urldesktop : require('../assets/images/desktop/image-gallery-milkbottles.jpg') ,   alt: 'milk bottle' },
                { id:2, urlmobile : require('../assets/images/mobile/image-gallery-orange.jpg')  , urldesktop : require('../assets/images/desktop/image-gallery-orange.jpg') ,   alt: 'orange' },
                { id:3, urlmobile : require('../assets/images/mobile/image-gallery-cone.jpg' ) , urldesktop : require('../assets/images/desktop/image-gallery-cone.jpg' ) , alt: 'cone' },
                { id:4, urlmobile : require('../assets/images/mobile/image-gallery-sugar-cubes.jpg')  , urldesktop : require('../assets/images/desktop/image-gallery-sugarcubes.jpg') ,   alt: 'sugar' }
          ]
      }
  }
}
</script>

<style lang="scss">
    .gallery{
        display: grid; 
        grid-template-columns: repeat(2, 1fr); 
        grid-template-rows: repeat(2, 1fr); 
        gap: 0px 0px;   
    }
    // Medium devices (tablets, 768px and up)
    @media (min-width: 768px) {
        .gallery{
            display: flex;
        }
    }


</style>
