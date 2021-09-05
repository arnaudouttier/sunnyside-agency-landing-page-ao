<template>
   <div class="testimonials" >
       <h3>Client testimonials</h3>
       <div class="testimonials-content">
         <TestimonialsCard />
       </div>
   </div>
</template>

<script>
import TestimonialsCard from './TestimonialsCard.vue'

export default {
  components: {
    TestimonialsCard,
  }
}
</script>

<style lang="scss" scoped>
    @import "./src/scss/variables.scss";
    
    .testimonials{
      padding: 60px 35px;
      text-align: center;
    }
     h3{
       margin-bottom: 70px;
        text-transform: uppercase;
        color: $grayish-blue;
        font-size: 1rem;
        letter-spacing: 0.282em;
    }

      // Medium devices (tablets, 768px and up)
    @media (min-width: 768px) {
      .testimonials{
        padding: 50px;
      }
      .testimonials-content{
        display: flex;
      }
    }
          // Medium devices (tablets, 768px and up)
    @media (min-width: 992px) {
        .testimonials{
          padding: 150px;
        }
      }
</style>
